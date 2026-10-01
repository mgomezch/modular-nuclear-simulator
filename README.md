# Modular Pressure Tube Reactor (MPTR) Simulator

An interactive, browser-based WebAssembly reactor simulator for the **Modular Nuclear** mod.

🔗 **Live Simulation Webapp**: [https://mgomezch.github.io/modular-nuclear-simulator/](https://mgomezch.github.io/modular-nuclear-simulator/)

---

## Overview

The MPTR Simulator models complex multi-chamber nuclear reactor physics, fluid dynamics, and turbine power generation entirely client-side in your web browser. 

The core simulation engine is transpiled from Java bytecode directly to **WebAssembly (WASM)**, providing exact physical parity with in-game calculations at simulation speeds exceeding 2,000 ticks/sec with 0ms network latency.

---

## Features

- **Real-Time Thermodynamics & Heat Transfer**:
  - Inter-tile thermal conduction, convection, and chamber heat dissipation.
  - Active coolant boiling for Distilled Water, High-Pressure Distilled Water, Heavy Water, and IC2 Coolant.
  - Boiling curve turnover kinetics with heat transfer and boiled dry safety states.

- **Neutron Kinetics & Transmutation**:
  - Individual fast and thermal neutron tracking per chamber tile.
  - Directional neutron scattering, moderator deceleration, and beryllium/carbon reflection.
  - Control rod neutron absorption and nuclear fuel breeding (including Tritium and Deuterium breeding).
  - Radiovoltaic cell direct energy generation from neutron capture.

- **Interactive Chamber Designer & Palette**:
  - Full tile palette with all nuclear fuels (Thorium, Uranium, MOX, Naquadah, Naquadria, Tiberium, and exotic rods).
  - Coolant hatches, heat vents, heat exchangers, and reflector components.
  - Live tile inspection detailing temperature, flux densities, and fluid turnover.

- **Power Estimation Pipeline**:
  - Multi-stage turbine power calculations for regular steam, superheated steam, and supercritical steam.
  - Large Steam Turbine (LST) and Extreme Large Steam Turbine (XLST) models with customizable rotor materials and sizing.
  - Cascading multi-stage heat exchanger modeling.

- **Four Display Modes**:
  - 🌡️ **Temperature Heatmap**
  - ⚛️ **Total Neutron Flux**
  - ⚡ **Fast Neutron Flux**
  - 🟢 **Thermal Neutron Flux**

---

## Technical Details

- **Engine**: Transpiled from Java bytecode using TeaVM to standalone WebAssembly.
- **Runtime**: Client-side WebAssembly with zero backend dependencies.
- **Hosting**: GitHub Pages.
