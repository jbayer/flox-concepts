# Flox Specifics

The [Concepts](concepts.md) page describes how Flox thinks about packages, dependencies, builds, environments, and upgrades. This page shows how those concepts work in practice with Flox.

## Flox Platform

The Flox platform has a client and server. The client is the [Flox CLI](https://flox.dev/download/) on each hsot where the client is installed. The server is called [FloxHub](https://hub.flox.dev) and is the web interface and APIs called by the CLI.

```mermaid
flowchart LR
    CLI[Flox CLI] <-->|Network| FH[FloxHub]
    CLI --> E[Environments]
    CLI --> B[Builds]
    FH --> C[Catalog]
    FH --> R[Remote Environments]
```

## Packages

Flox maintains a Catalog that is derived from the 120,000+ packages in Nixpkgs -- one of the largest curated package sets available. Each package is identified by name and version, and every version is built reproducibly so that installing a package produces the same result everywhere. You can also build and publish your own packages to the Flox Catalog.

Because packages are pre-built and cached, installation is fast -- Flox downloads the result rather than building from source.

```mermaid
flowchart LR
    N[Nixpkgs] --> C[Flox Catalog]
    U[Custom Packages] --> C
```

## Dependencies

When you install a package, Flox automatically resolves its full dependency graph. Every library, runtime, and tool that the package needs is included -- pinned to exact versions maintained in a lockfile. You do not manually manage transitive dependencies; Flox guarantees that the resolved graph is complete and consistent.

```mermaid
flowchart TD
    N[nodejs] --> O[openssl]
    N --> Z[zlib]
    N --> L[libuv]
    O --> Z
```

This means two people installing the same package get exactly the same dependency tree -- not just the same top-level version, but the same versions of everything underneath.

## Builds

Flox builds packages in an isolation using Nix. Each build runs in a sandbox with only its declared inputs available -- no network access, no untracked files from disk, no ambient system state. This is what makes builds reproducible: if the inputs have not changed, the output is identical.

The path to each output is derived from the prefix `/nix/store` and a hash of its inputs, so two builds with the same inputs always produce the same path. This enables confident caching and sharing -- if the hash matches, the output is guaranteed identical.


```mermaid
flowchart LR
    subgraph Sandbox
        S[Source + Deps] --> B[Build]
    end
    B --> H[Input-Addressed Output]
```


## Environments

A Flox environment is defined by a `manifest.toml` file that declares the packages, configuration, environment variables, and shell hooks for a project. When you or a teammate activate the environment, Flox resolves the manifest and produces the same result. Flox CLI imperative commands will create and maintain the environment's `manifest.toml` for you when you run commands like.

```
flox init
flox install nodejs python3
flox uninstall nodejs
```

The manifest is checked into version control alongside your code. Anyone who clones the repository and runs `flox activate` gets the same tools at the same versions. Environments can also be shared via FloxHub without requiring a shared repository.

```mermaid
flowchart LR
    T[manifest.toml] --> R[Resolve]
    R --> E[Environment]
    E --> P1[nodejs]
    E --> P2[python3]
    E --> V[ENV Variables]
    E --> H[Shell Hooks]
```

## Upgrades

Flox environments are versioned. Each change to the manifest -- adding a package, removing one, or upgrading a version -- creates a new generation. You can upgrade packages and, if something breaks, roll back to any previous generation instantly.

```
flox upgrade nodejs
flox list --generations
flox rollback
```

Because each generation is a complete snapshot of the resolved environment, rollback is not an undo -- it is switching to a known-good state that still exists.

```mermaid
flowchart LR
    G1[Generation 1] --> U[Upgrade]
    U --> G2[Generation 2]
    G2 --> RB[Rollback]
    RB --> G1
```
