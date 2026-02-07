# Fork / Branch Note

This fork / branch simply takes [this PR](https://github.com/BillyDM/iced_baseview/pull/43)
And points at iced 0.14 instead of its main branch.

The main explanation for this can be [found in my other repo](https://github.com/chairbender/nih-plug)

Original readme follows below...

# `iced_baseview`

![Test](https://github.com/BillyDM/iced_baseview/workflows/Rust/badge.svg)
[![Crates.io](https://img.shields.io/crates/v/iced_baseview.svg)](https://crates.io/crates/iced_baseview)
[![License](https://img.shields.io/crates/l/iced_baseview.svg)](https://github.com/BillyDM/iced_baseview/blob/main/LICENSE)

A [baseview] backend for the [Iced] GUI library

<div align="center">
    <img src="screenshot.png">
</div>

The [main branch](https://github.com/BillyDM/iced_baseview/tree/main) of this repository tracks the latest crates.io release of iced, while [iced_git  branch](https://github.com/BillyDM/iced_baseview/tree/iced_git) tracks its git repository.

## VST3 / CLAP / AU Plugins

Examples of how to use this library for audio plugins can be found here:
* [nih_plug_iced](https://github.com/robbert-vdh/nih-plug/tree/master/nih_plug_iced)
* [iced-baseplug-examples](https://github.com/BillyDM/iced-baseplug-examples)

[Iced]: https://github.com/hecrj/iced
[baseview]: https://github.com/RustAudio/baseview
