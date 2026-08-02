<p align="center">
  <!-- Replace docs/logo.png with your Barysta logo -->
  <img src="barysta_logo.png" alt="Barysta logo" width="220"/>
</p>

<h1 align="center">Barysta</h1>

<p align="center"><em>A toy RTL integrator — stitching blocks together, one shot at a time.</em></p>

<p align="center"><strong>Written in Racket.</strong></p>

---

## Overview

**Barysta** is a toy RTL integrator built to learn how digital design tooling
works from the inside out. Given a set of RTL blocks and a description of how
they connect, an integrator assembles a top-level design: instantiating
submodules, wiring up ports and buses, resolving parameters, and emitting a
structural top-level netlist.

This is a learning project, not a production tool. It's written in **Racket** on
purpose — RTL integration is essentially a compiler front end (parse interfaces,
build an IR, run passes, emit a netlist), and Racket is a language built for
building languages. S-expressions make a natural IR, macros make emitting
structural HDL pleasant, and REPL-driven development suits a design that's still
taking shape.

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

- **Racket** (DrRacket for interactive development)
- **`raco`** for building and package management

Once there's code, the intended workflow will look roughly like:

```bash
raco pkg install --deps search-auto
racket barysta.rkt
```
---

*Part of a small suite of toy EDA tools built for learning.*
