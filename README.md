# Pulse Configurator

This is a simple web-based application for creating pulse sequences (Bias and measurement waveforms) for the Polaris System at the IITB NanoFab. It can produce CSV and excel file outputs of applied voltages and measurement schemes of both standard and custom waveforms.

### !!! Bugs may be present since I have not maintained the tool. Use at your own discretion.

# Details

A browser-based tool for designing, visualizing, and exporting piecewise-linear voltage pulse sequences with configurable measurement schemes.

Pulse Configurator helps generate pulse waveforms for multi-probe measurement setups by providing an interactive interface for configuring Gate (G), Drain (D), Source (S), and Bulk (B) signals, defining timing parameters, and exporting generated tables for external analysis software.

## Features

### Pulse Configuration

* Configure independent waveforms for:

  * Gate (G)
  * Drain (D)
  * Source (S)
  * Bulk (B)

* Supported probe modes:

  * Constant voltage
  * Pulsed waveform
  * Multi-pulse waveform

* Adjustable pulse parameters:

  * Pulse duration
  * Number of repeats
  * Pulse voltage
  * Voltage sweep across cycles
  * Rise and fall times
  * Timing gaps
  * Number of cycles
  * Base voltage

## Measurement Schemes

The application supports two measurement generation modes:

### Linear Measurement Scheme

Creates a uniform measurement sequence using:

* Integration cycle time (`t_cycle`)
* Average/high measurement time (`t_high`)
* Maximum points per row
* Current range
* Voltage range

### Smart Measurement Scheme

Allows measurement configuration on individual waveform segments.

Features:

* Segment browser for waveform regions
* Per-segment measurement rows
* Custom offsets within segments
* Configurable:

  * Number of points
  * Measurement cycle time
  * High measurement time
  * Low measurement time

Built-in budget monitoring tracks:

* Measurement rows
* Total measurement points
* Pulse sequence points

## Custom Waveform Mode

The custom waveform editor allows manual waveform creation.

Capabilities:

* Add waveform nodes
* Move waveform points
* Delete nodes
* Snap points to grid
* Edit segment values precisely
* Visualize waveform changes interactively

## Export

Generated data can be exported independently for each probe:

* Gate CSV
* Drain CSV
* Source CSV
* Bulk CSV

Additional export features:

* Copy tables as text
* Copy formatted tables for spreadsheet/software use


## Usage

1. Open at https://kartikuc.github.io/pulser/
2. Select the operating mode:

   * Configurator
   * Custom waveform
3. Configure probe waveforms.
4. Select a measurement scheme.
5. Generate and review waveform outputs.
6. Export CSV files or copy tables for external tools.

## Limits

The application includes validation limits for:

* Minimum timing values
* Maximum measurement rows
* Maximum measurement points
* Maximum pulse sequence points

These limits help keep generated measurement sequences within supported operating ranges.




