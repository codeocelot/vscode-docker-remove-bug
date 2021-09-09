# Reproduction of bug found in VSCode Docker extension

In brief, it seems `dockerRun.remove` has no effect.  Whether or not this flag is enabled, disabled or not specified, the container will always be removed after it's completed or the parent task is cancelled.

## How to use

There are two launch commands to start a trivial container that differ only in that they call two different tasks, who are identical save for `dockerRun.remove`.  Note how in both cases, the container is always removed.

