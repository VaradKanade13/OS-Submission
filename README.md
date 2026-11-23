# OS-Submission
3rd Semester Operational system complete submission

# A overview for CA2, CA3, CA5


CA-2 — Page Replacement Performance Investigation: Built a Python 3.13 discrete-event simulator evaluating FIFO, LRU, and Optimal (OPT) across 5 workloads (Uniform Random, 50-page Sequential Loop, Skewed 80/20, Phased 90% with WS=8, and Phased 100% with WS=8), 5 frame counts (m in {4, 8, 16, 32, 64}), and 5 seeds (375,000 references total).

CA-3 — Page Replacement Design & Debugging Challenge: Diagnosed and modeled Belady's Anomaly in FIFO (9 to 10 faults from 3 to 4 frames), cyclic loop cache thrashing (100% fault rate for m less than or equal to 32 on a 50-page loop), and working-set thrashing (m less than WS=8). Implemented an O(1) OrderedDict LRU engine and verified across 5 test categories and a before/after regression audit.

CA-5 — Linux Virtual Memory Engineering Challenge: Correlated simulation behavior with Linux kernel telemetry (/proc/meminfo, /proc/<pid>/statm, vmstat, pidstat, resource.getrusage(), and cgroups v2) on Ubuntu 24.04 LTS / Linux 6.6.x (WSL2). Tuned vm.swappiness=10 and vm.vfs_cache_pressure=50, applied scan-resistant queue partitioning concepts, and used cgroups v2 memory.max limits to protect working sets.

file:///C:/Users/Varad/Downloads/Operating%20Systems%20Projects%20Summary.pdf


# A OVERVIEW OF MICRO OS

1. Rust Micro-OS

A minimal x86_64 operating system / microkernel built in Rust and tested in Oracle VirtualBox.

2. Overview

This repository contains the bootloader/kernel setup, low-level hardware initialization, and experimental OS components developed in Rust for virtualized x86_64 execution.

3. Key Features & Focus Areas

- **Rust Systems Programming:** Low-level boot hand-off, memory/paging structures, and interrupt/hardware handling in Rust.
- **VirtualBox Testing:** Built and booted inside VirtualBox to iterate quickly on kernel behavior, console output, and system primitives.
- **OS Experiments:** Exploration of core OS concepts such as scheduling, memory management, and page-replacement algorithms.

# Getting Started

4. Prerequisites

- **Rust Toolchain** (`rustup`, `cargo`, and appropriate `x86_64` / `no_std` target components)
- **Oracle VirtualBox** (for running and testing the bootable image)

5. Build & Run in VirtualBox

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
