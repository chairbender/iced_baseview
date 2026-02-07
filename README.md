# Fork / Branch Note

This fork / branch simply takes [this PR](https://github.com/BillyDM/iced_baseview/pull/43)
And points at iced 0.14 instead of its main branch.

The main explanation for this can be [found in my other repo](https://github.com/chairbender/nih-plug)

# Additional Changes
Not sure why, but even with the PR I based this on, there were some issues when using
the real iced 0.14 branch that I addressed...
* lib.rs: iced_runtime::futures::keyboard event handling was changed to match iced 0.14
    which changed how [keyboard events are handled](https://github.com/iced-rs/iced/commit/7e5b6f6802ae244676b5d692b3c496893e33b3c6#diff-80ae69e81543d1e456d4cabf5515089086281f0d499e15edb0e3b61a779dfc60)
* Fix f32 / f64 type mismatch when dealing with Viewports. Simply downcast to f32 
  (not sure if that's the BEST way but it's a start)
* Theme in iced no longer implements Default, so removed Default bound from Application::Theme. I'm guessing
  this isn't the best approach since now it would require the Theme to always be specified - probably Optional is better.
* Refactored a few various changes in iced APIs where the way of constructing / building different structs was changed.
* Some various switch statements were missing arms, which are added (currently just todos, IDK what they should be)
* keyboard event requires specifying repeat: true/false. I just left it as false for now.
* 

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
