# Overconsumption Calculator

WPF tool that assesses engine fuel over- or under-consumption against a
reference (ISO) consumption, based on shaft/engine RPM and torque.

## Overview

Using the engine's reference RPM, power and ISO fuel-consumption data, the tool
evaluates the actual consumption at the measured operating point - from a volume
or mass flowmeter - and reports whether the engine is over- or under-consuming.

## Features

- Reference engine curves (RPM, power, ISO FOC)
- Volume or mass flowmeter input
- Interpolation of the reference curve (MathNet.Numerics)
- Deviation result

## Tech stack

- WPF, .NET Core 3.1 (Windows Desktop SDK)
- MathNet.Numerics, Xceed WPF DataGrid

## Repository layout

```
WPF_Overconsumption/
  ConsumptionCalc.cs
  Helpers/   interpolation, converters
  MainWindow.xaml / .cs
WPF_Overconsumption.sln
OVERCONSUMPTION BASED ON TC RPM.xls   reference spreadsheet
```

## Notes

The reference spreadsheet `OVERCONSUMPTION BASED ON TC RPM.xls` in the
repository root documents the calculation basis.
