# fedora-minimal

Fedora Minimal Template in Qubes OS.

## Table of Contents

* [Description](#description)
* [Installation](#installation)
* [Usage](#usage)


## Description

Creates the Fedora Minimal template as well as a Disposable Template based on
it.

## Installation

- Top:
```sh
sudo qubesctl top.enable fedora-minimal
sudo qubesctl --targets=fedora-39-minimal state.apply
sudo qubesctl top.disable fedora-minimal
```

- State:
<!-- pkg:begin:post-install -->
```sh
sudo qubesctl state.apply fedora-minimal.create
sudo qubesctl --skip-dom0 --targets=fedora-39-minimal state.apply fedora-minimal.install
```
<!-- pkg:end:post-install -->

## Usage

AppVMs and StandaloneVMs can be based on this minimal template.
