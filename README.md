<p align="center">
  <!-- Replace docs/logo.png with your Barysta logo -->
  <img src="barysta_logo.png" alt="Barysta logo" width="220"/>
</p>

<h1 align="center">Barysta</h1>

<p align="center"><em>A toy RTL integrator — stitching blocks together, one order at a time.</em></p>

---

## Overview

**Barysta** is a toy RTL integrator built to learn how digital design tooling
works from the inside out. Given a set of RTL blocks and a description of how
they connect, an integrator assembles a top-level design: instantiating
submodules, wiring up ports and buses, resolving parameters, and emitting a
structural top-level netlist.

This is a learning project, not a production tool. The goal is to understand the
mechanics — parsing module interfaces, building a connectivity graph, and
generating correct structural RTL — by implementing them by hand.

## Status

🌱 **Very early.** No code yet. This repo currently exists to reserve the name
and capture intent. Expect it to sit quietly for a while before the first commit.

## Planned scope

- Parse module interface definitions (ports, widths, directions, parameters)
- Represent a design as a connectivity graph of instances and nets
- Resolve parameterization and elaborate the hierarchy
- Detect obvious wiring mistakes (width mismatches, dangling ports, direction conflicts)
- Emit a structural top-level netlist

Nothing here is fixed — it's a sketch to aim at.

## Toolchain

- **Python 3.14**
- **[uv](https://github.com/astral-sh/uv)** for environment and dependency management

Once there's code, the intended setup will look roughly like:

```bash
uv python install 3.14
uv sync
```
---

*Part of a small suite of toy EDA tools built for learning.*
