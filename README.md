# Custom Code Block Modules for PEKAT Vision

A curated collection of custom Code Block modules designed to extend the core functionality of **PEKAT Vision**.

This repository serves as a centralized hub for pre-built, reusable scripts and custom logic developed to streamline vision inspection workflows and accelerate integration processes.

---

> ⚠️ **Disclaimer**  
> This repository is an **unofficial** collection maintained and developed by the **Škoda FabLab** team. It is not officially affiliated with, endorsed by, or supported by PEKAT Vision.

---

## Available `.ptool` scripts

The following Code Block modules are available for download and import into PEKAT Vision:

| Module | Description |
|---|---|
| [`AI_TRIGGER2_V07.ptool`](./AI_TRIGGER2_V07.ptool) | Releases a configurable number of frames after a debounce condition is met and resets the saturated state after a defined interval. |
| [`AI_TRIGGER2_V08.ptool`](./AI_TRIGGER2_V08.ptool) | Updated version of the AI trigger module. Releases a configurable number of frames after a debounce condition is met and resets the saturated state after a defined interval. |
| [`Classifier2Context.ptool`](./Classifier2Context.ptool) | Stores the classifier result in `globalData -> classifier_result`. The target variable name can be changed in the module form. |
| [`GUI_Maják_v04.ptool`](./GUI_Maják_v04.ptool) | Communicates with the PEKAT Vision GUI and supports control of an external signal tower through the PEKAT communication interface. |
| [`Rectangle_Mazator_v01.ptool`](./Rectangle_Mazator_v01.ptool) | Debug and filtering module for deleting or filtering detected rectangles. |
| [`Ukladator_v02.ptool`](./Ukladator_v02.ptool) | Saves captured images to the configured filesystem location, including timestamp-based organization. |
| [`Vyhodnocovator - New.ptool`](./Vyhodnocovator%20-%20New.ptool) | Evaluates whether the configured items are present and returns **OK** when they are, otherwise **NoK**. |
| [`Vypisovator_v03.ptool`](./Vypisovator_v03.ptool) | Draws custom text, a timestamp, and an optional transparent watermark directly into the image. Supports configurable position, color, scale, thickness, transparency, and background highlighting. |

> ℹ️ The descriptions are based on the module metadata and may not cover every available configuration option. Open the individual `.ptool` file for the complete module definition and form configuration.

---

### Key Features

* **Modular Integration:** Drop-in code blocks tailored for various PEKAT Vision processing pipelines.
* **Tested & Maintained:** Internal solutions refined and deployed for practical manufacturing and vision inspection scenarios.
* **Versioned Releases:** Pre-packaged modules ready for direct deployment in production environments.

---

### License

Distributed under the Apache License 2.0. See [`LICENSE`](./LICENSE) for more information.
