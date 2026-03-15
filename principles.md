# Principles

These principles are deeply ingrained in our beliefs and Flox. Understanding them will help you understand why Flox works the way it does and where it is going from here.

## Reproducibility

Same inputs, same results -- and you can prove it.

When you set up software, the result should be predictable. If you and a colleague start from the same description of what's needed, you should end up with the same thing -- every time, on every machine. This is not just about convenience. It is about removing an entire class of problems where something works in one place but not another. Confidence comes from verification, so it is essential that each step in the process is verifiable.

## Efficiency

Do work once. Repeatably reuse the results.

Building and configuring software takes time. Much of that time is spent repeating work that has already been done -- recompiling the same code, re-downloading the same dependencies, storing duplicate copies of something on-disk, re-running the same setup steps. If work is done once and the results are stored for reuse, every subsequent setup becomes faster. Teams spend less time waiting and more time on the work that matters.

## Simplicity

Managing the software you work with should be straightforward.

Setting up a project, making changes, sharing your setup with a teammate, upgrading a dependency, or rolling back a mistake -- none of these should require deep expertise or carry high risk. When common tasks are simple and safe, people are more willing to keep things up to date, experiment with improvements, and collaborate without friction.

---

These principles guide Flox concepts like environments, packages, and dependency management. To see how they translate into practice, continue to [Concepts](concepts.md).
