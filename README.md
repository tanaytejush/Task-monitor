# Task-monitor

A small C++ program that prints live CPU and memory usage on Linux, refreshing in a loop.

## Features

- **Memory usage**: reads total and free RAM through `sysinfo()` and prints the used amount in MB.
- **CPU usage**: reads the first line of `/proc/stat`.

## Status

This is an early prototype. Memory reporting works, but the CPU calculation in `getCPUUsage()` is still a placeholder and always reports `0%`. Parsing `/proc/stat` and comparing two samples is the next step.

## Requirements

- Linux (uses `/proc/stat` and `<sys/sysinfo.h>`)
- A C++ compiler such as `g++`

## Build and run

```bash
g++ main.cpp -o task-monitor
./task-monitor
```

Stop it with `Ctrl+C`.

## Roadmap

- [ ] Implement the CPU usage calculation from `/proc/stat`
- [ ] Per-process listing
- [ ] Configurable refresh interval


---

<sub>Made by [tanaytejush](https://github.com/tanaytejush)</sub>
