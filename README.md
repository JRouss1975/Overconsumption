# Overconsumption Calculator

Windows desktop tool that assesses engine fuel **over- or under-consumption**
against the reference (ISO) consumption at the measured engine operating point.

---

## At a glance

| | |
| --- | --- |
| **Type** | Windows desktop app (WPF) |
| **Built with** | C# · .NET Core 3.1 (`netcoreapp3.1`) |
| **Status** | Stable: no recent changes (published May 2022) |

---

## Features

- **Reference engine curves:** RPM, power and ISO fuel oil consumption.
- **Flowmeter input** by volume or by mass.
- **Interpolation** of the reference curve at the measured operating point (MathNet.Numerics).
- **Result:** deviation from the reference consumption, flagged as over- or under-consumption.

---

## Requirements

| | |
| --- | --- |
| Operating system | Windows 10 or 11 |
| Build | Visual Studio 2019 or 2022 with the **.NET desktop development** workload and the .NET Core 3.1 SDK |

> .NET Core 3.1 is out of support. To build with a current SDK, change `TargetFramework`
> in `WPF_Overconsumption.csproj` to `net8.0-windows`.

---

## Building and running

1. Open `WPF_Overconsumption.sln` in Visual Studio.
2. NuGet packages restore automatically on the first build.
3. Build and run with **F5**.

---

## Project structure

```
WPF_Overconsumption.sln
WPF_Overconsumption/
├─ ConsumptionCalc.cs       calculation model
├─ Helpers/                 interpolation and converters
└─ MainWindow.xaml(.cs)     main window
OVERCONSUMPTION BASED ON TC  RPM.xls   reference spreadsheet
```

---

## Dependencies

| Package | Used for |
| --- | --- |
| MathNet.Numerics | Curve interpolation |
| Xceed.Wpf.DataGrid | Data grid |

---

## Documentation

The spreadsheet `OVERCONSUMPTION BASED ON TC  RPM.xls` in the repository root
documents the calculation basis.

---

## License

Copyright © JRouss1975. All rights reserved.

No license is granted to use, copy, modify or distribute this code without written permission.
