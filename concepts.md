# Concepts

The [Principles](principles.md) describe *why* reproducibility, efficiency, and simplicity matter. The concepts below introduce how Flox puts the principles into practice.

## Packages

Packages are pre-built, versioned units of software ready to use.

A package is a single piece of software -- a tool, a library, a runtime -- that has been built, tested, and stored so it can be installed reliably.

```mermaid
flowchart LR
    S[Source] --> B[Build]
    B --> P[Package]
```

## Dependencies

Dependencies are relationships between packages represented as a graph.

Software rarely stands alone. A tool may require a specific library, which in turn requires another. Dependencies describe the relationships between packages and each package version as a directed graph. 

```mermaid
flowchart TD
    L1[Package A]
    L2[Package B]
    L1 --> C[Package C]
    L2 --> C
```

## Builds

Builds consist of package inputs that are processed together and create package outputs.

Inputs are source code, configuration, environment variables, compiler flags, and dependencies on the outputs from other packages. Outputs are executable binaries, libraries, scripts, and other similar results of performing a build. 

```mermaid
flowchart LR
    subgraph Inputs
        S[Source Code]
        C[Config & Flags]
        D[Dependencies]
    end
    subgraph Outputs
        B[Binaries]
        L[Libraries]
        SC[Scripts]
        M[Man Pages]
    end
    Inputs --> I[Build]
    I --> Outputs
```

## Environments

Environments are complete, portable descriptions of software.

An environment represents the graph of packages, configuration, and scripting required to use the environment. Instead of each person installing software by hand and hoping the versions match, the environment describes what is needed and produces the same result everywhere.

```mermaid
flowchart LR
    E[Environment] --> P1[Package A]
    E --> P2[Package B]
    E --> P3[Configuration]
```

## Upgrades

Upgrades are safe, reversible changes to your software.

Upgrading means building new versions of packages, and updating environments to use those updated versions. If an upgrade causes a problem, roll back to a known-good state.

```mermaid
flowchart LR
    V1[Version 1] --> U[Upgrade]
    U --> V2[Version 2]
    V2 --> R[Rollback]
    R --> V1
```

## Flox Platform

The concepts above are implemented in Flox as a complete platform for software lifecycle management. To see how they work in practice with specific commands and examples, continue to [Flox Platform](flox.md).
