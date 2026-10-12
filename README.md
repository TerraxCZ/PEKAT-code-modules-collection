# Custom Code Block Modules for PEKAT Vision

A curated collection of custom Code Block modules designed to extend the core functionality of **PEKAT Vision**.

This repository serves as a centralized hub for pre-built, reusable scripts and custom logic developed to streamline vision inspection workflows and accelerate integration processes.

[![Latest Release](https://img.shields.io/github/v/release/TerraxCZ/PEKAT-code-modules-collection?style=for-the-badge&color=78faae)](https://github.com/TerraxCZ/PEKAT-code-modules-collection/releases/latest)
![Last Commit](https://img.shields.io/github/last-commit/TerraxCZ/PEKAT-code-modules-collection?style=for-the-badge&color=78faae)

[👉 Stáhnout nejnovější verzi (.zip)](https://github.com/TerraxCZ/PEKAT-code-modules-collection/releases/latest)

---

> ⚠️ **Disclaimer**  
> This repository is an **unofficial** collection maintained and developed by the **Škoda FabLab** team. It is not officially affiliated with, endorsed by, or supported by PEKAT Vision.

---

## 🚀 How to Use Modules

All `.pmodule` and `.ptool` blocks in this repository are built with simplicity and reusability in mind:

> 💡 **No coding required:** You can simply import any module and configure its parameters directly through the user interface forms—without ever opening or modifying the underlying Python code.

### Importing a module into PEKAT Vision:

1. In PEKAT Vision, click **Add tool** $\rightarrow$ **Import** $\rightarrow$ **code**.
2. Select the desired `.pmodule` or `.ptool` file from this collection.
3. Configure the parameters in the right-hand tool panel (e.g., timers, thresholds, context variables, or custom text) to match your application requirements.

---

## 📦 Available Modules

The collection contains both `.ptool` and `.pmodule` Code Block modules. They are not separated by purpose, but by PEKAT Vision compatibility:

- **`.ptool` modules** are the newer format and are **not backward-compatible with PEKAT Vision versions below 4.0**.
- **`.pmodule` modules** are forward-compatible and can also be used with newer PEKAT Vision versions.

| Module | Description |
|---|---|
| [`AI_TRIGGER2_V08.ptool`](./AI_TRIGGER2_V08.ptool) | Releases a configurable number of frames after a debounce condition is met and resets its saturated state after a defined interval. This module is ideal for preventing redundant capturing—for example, saving just a single image per workpiece on a conveyor belt rather than taking thousands of duplicate photos when a part stops or stays overnight. You can configure a debounce condition (e.g., requiring the classifier result "part" 3 times consecutively) to trigger frame release, and set a reset delay based on belt movement before the module is ready for the next part.This is the newer .ptool version of the AI trigger module.|
| [`BUFFER.pmodule`](./BUFFER.pmodule) | Buffers and stores image data for later processing. The module supports configurable buffering behavior and file handling for image sequences. |
| [`Classifier2Context.ptool`](./Classifier2Context.ptool) | Stores classifier results in context data so that detected objects can be compared programmatically with externally acquired data. It was created for comparing detected objects with data from the Sofist system and is intended primarily as an example or source of inspiration rather than as a universal solution. |
| [`GUI_Maják_v04.ptool`](./GUI_Maják_v04.ptool) | Controls an **IFM DV2131 signal tower** through the PEKAT Vision GUI and communication interface. |
| [`Rectangle_Mazator_v01.ptool`](./Rectangle_Mazator_v01.ptool) | A debugging and filtering module for working with detected rectangles. It was created to visualize object detector rectangles without also drawing the full-screen classifier rectangle, which could otherwise tint the entire image with the classifier rectangle's color. |
| [`Ukladator_v02.ptool`](./Ukladator_v02.ptool) | A custom image-saving script created because the native PEKAT Vision image saver did not provide sufficient reliability or functionality. It supports extended options such as image compression, heatmap colormap and alpha, rectangle thickness and alpha, configurable filename and date formats, limiting the number of stored images, and more. |
| [`Vyhodnocovator - New.ptool`](./Vyhodnocovator%20-%20New.ptool) | Evaluates sets of detected objects against a predefined list using set operations. Originating from the same project as Classifier2Context, it allows users to set a threshold for how many missing objects are still acceptable for an OK result. For more complex, custom evaluation rules, the underlying code can be easily extended or modified. |
| [`Vykreslovator_v01.pmodule`](./Vykreslovator_v01.pmodule) | A debugging tool for tracing an image's path through the PEKAT Vision structure. Since PEKAT Vision does not provide a native way to highlight which branch an image passed through, the module can be placed in each parallel branch and configured to draw a differently colored dot in a different image position. The resulting image makes it possible to determine which path the image took. |
| [`Vypisovator_v03.ptool`](./Vypisovator_v03.ptool) | Adds customizable stamps and watermarks to the image. Users can independently enable and combine any of the following elements: a timestamp (with configurable format), a fixed message, custom image context variables, or a watermark logo. The position and alpha transparency of each selected element are fully configurable. |

> ℹ️ The descriptions are concise summaries and may not cover every available configuration option. Open the individual module file for the complete module definition and form configuration.

---

### Key Features

* **Modular Integration:** Drop-in Code Blocks tailored for various PEKAT Vision processing pipelines.
* **Practical Manufacturing Use:** Internal solutions refined and deployed for real-world vision inspection scenarios.
* **Extended Functionality:** Custom tools for debugging, visualization, data comparison, image storage, and external hardware control.
* **Versioned Releases:** Pre-packaged modules ready for direct deployment where the relevant PEKAT Vision version is supported.

---

### License

Distributed under the Apache License 2.0. See [`LICENSE`](./LICENSE) for more information.
![License](https://img.shields.io/github/license/TerraxCZ/PEKAT-code-modules-collection)
