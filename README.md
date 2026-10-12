# Custom Code Block Modules for PEKAT Vision

A curated collection of custom Code Block modules designed to extend the core functionality of **PEKAT Vision**.

This repository serves as a centralized hub for pre-built, reusable scripts and custom logic developed to streamline vision inspection workflows and accelerate integration processes.

---

> ⚠️ **Disclaimer**  
> This repository is an **unofficial** collection maintained and developed by the **Škoda FabLab** team. It is not officially affiliated with, endorsed by, or supported by PEKAT Vision.

---

## Available modules

The collection contains both `.ptool` and `.pmodule` Code Block modules. They are not separated by purpose, but by PEKAT Vision compatibility:

- **`.ptool` modules** are the newer format and are **not backward-compatible with PEKAT Vision versions below 4.0**.
- **`.pmodule` modules** are forward-compatible and can also be used with newer PEKAT Vision versions.

| Module | Description |
|---|---|
| [`AI_TRIGGER2_V08.ptool`](./AI_TRIGGER2_V08.ptool) | Releases a configurable number of frames after a debounce condition is met and resets the saturated state after a defined interval. This is the newer `.ptool` version of the AI trigger module. |
| [`BUFFER.pmodule`](./BUFFER.pmodule) | Buffers and stores image data for later processing. The module supports configurable buffering behavior and file handling for image sequences. |
| [`Classifier2Context.ptool`](./Classifier2Context.ptool) | Stores classifier results in context data so that detected objects can be compared programmatically with externally acquired data. It was created for comparing detected objects with data from the Sofist system and is intended primarily as an example or source of inspiration rather than as a universal solution. |
| [`GUI_Maják_v04.ptool`](./GUI_Maják_v04.ptool) | Controls an **IFM DV2131 signal tower** through the PEKAT Vision GUI and communication interface. |
| [`Rectangle_Mazator_v01.ptool`](./Rectangle_Mazator_v01.ptool) | A debugging and filtering module for working with detected rectangles. It was created to visualize object detector rectangles without also drawing the full-screen classifier rectangle, which could otherwise tint the entire image with the classifier rectangle's color. |
| [`Ukladator_v02.ptool`](./Ukladator_v02.ptool) | A custom image-saving script created because the native PEKAT Vision image saver did not provide sufficient reliability or functionality. It supports extended options such as image compression, heatmap colormap and alpha, rectangle thickness and alpha, configurable filename and date formats, limiting the number of stored images, and more. |
| [`Vyhodnocovator - New.ptool`](./Vyhodnocovator%20-%20New.ptool) | Originating from the same project as `Classifier2Context`, this module compares a set of detected objects stored in context with a predefined, currently hardcoded set and performs set operations on them. The current implementation is intended for project-specific evaluation and does not yet cover every desired condition, such as all `2 > OK` cases. |
| [`Vykreslovator_v01.pmodule`](./Vykreslovator_v01.pmodule) | A debugging tool for tracing an image's path through the PEKAT Vision structure. Since PEKAT Vision does not provide a native way to highlight which branch an image passed through, the module can be placed in each parallel branch and configured to draw a differently colored dot in a different image position. The resulting image makes it possible to determine which path the image took. |
| [`Vypisovator_v03.ptool`](./Vypisovator_v03.ptool) | Adds a stamp to the image, including a constant message and a timestamp with a configurable format. With code changes, variable information from the image context can also be displayed. The module can additionally place a watermark in the image, with configurable position and alpha for the rendered elements. |

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
