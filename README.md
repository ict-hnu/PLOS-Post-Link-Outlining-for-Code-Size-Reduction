# PLOS: Post-link Outlining for Code Size Reduction

## Introduction

This repository is associated with the paper **"Post-link Outlining for Code Size Reduction"**, which presents a novel approach for reducing the size of compiled binaries through a post-link optimization technique.

Code size reduction is particularly important for resource-constrained environments such as embedded systems and IoT devices, where memory and storage are limited. Our method leverages **post-link outlining** to identify and extract repeated instruction sequences across the entire binary, creating reusable outlined functions that replace the original sequences.

Unlike traditional compiler-stage optimizations, this process takes place **after linking**, enabling whole-program analysis while remaining compatible with different compiler front-ends and intermediate optimizations.

The input to our approach is a **binary executable file**, and the output is an **optimized binary executable file** with reduced code size. This repository provides the implementation of our approach, together with the scripts and instructions needed to reproduce the results presented in the paper.

## Paper and Artifact

- **Paper**: [Post-link Outlining for Code Size Reduction](https://dl.acm.org/doi/10.1145/3708493.3712692)
- **Artifact**: [Zenodo Artifact Package](https://zenodo.org/records/14689800)

## Artifact Requirements

### 1. Operating System and Architecture
- **Operating System**: Ubuntu 22.04
- **Architecture**: AArch64

The artifact has not been validated on other operating systems or architectures. For the best compatibility, we recommend using the configuration above.

### 2. Hardware Requirements
- **Memory**: At least 8 GB RAM
- **Storage**: At least 64 GB available disk space
- **CPU**: AArch64 processor, recommended clock speed 2.2 GHz or higher

### 3. Environment and Tools
- Linux environment
- `make` installed and available in `PATH`
- `perf` installed with sufficient permissions to run
- Python environment with the following libraries:
  - `os`
  - `re`
  - `subprocess`
  - `argparse`
  - `openpyxl` (including `Workbook` and `load_workbook`)

## Usage Guide

### 1. Extract the Artifact Package

First, extract the artifact package:

```bash
tar -xzvf artifact_PLOS.tar
