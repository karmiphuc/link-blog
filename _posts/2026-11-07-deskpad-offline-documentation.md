---
layout: post
title: "DeskPad: offline screen-sharing setup and troubleshooting"
summary: "A text-only preservation of the MIT-licensed DeskPad README, including installation, display setup and permission troubleshooting."
date: 2026-11-07
tags: ["Tools", "OfflineArchive"]
---

**Licensed documentation archive.** Checked 2026-11-07 UTC.

Source: [DeskPad](https://github.com/Stengo/DeskPad), Bastian Andelefski and contributors. Captured README: [revision c3349f0e](https://github.com/Stengo/DeskPad/blob/c3349f0e237e000cb4826fb3ea1cdd1c44949461/README.md). Reuse basis: [MIT License](https://github.com/Stengo/DeskPad/blob/c3349f0e237e000cb4826fb3ea1cdd1c44949461/LICENSE.md), reproduced below.

Coverage and changes: the complete README prose, commands and troubleshooting steps are retained below. Three decorative image blocks were omitted and headings demoted for this post. No application binaries or screenshots are archived; no installation was performed. The text is usable offline, but a fresh installation still needs a separately obtained release or Homebrew network access.

## DeskPad
A virtual monitor for screen sharing

Certain workflows require sharing the entire screen (usually due to switching through multiple applications), but if the presenter has a much larger display than the audience it can be hard to see what is happening.

DeskPad creates a virtual display that is mirrored within its application window so that you can create a dedicated, easily shareable workspace.

## Installation
You can either download the [latest release binary](https://github.com/Stengo/DeskPad/releases) or install via [Homebrew](https://brew.sh) by calling `brew install --cask deskpad`.

## Usage
DeskPad behaves like any other display. Launching the app is equivalent to plugging in a monitor, so macOS will take care of properly arranging your windows to their previous configuration.

You can change the display resolution through the system preferences and the application window will adjust accordingly.

Whenever you move your mouse cursor to the virtual display, DeskPad will highlight its title bar in blue and move the application window to the front to let you know where you are.

## Troubleshooting
DeskPad may need screen recording permissions to display properly. Follow these steps:

1. **Open System Settings** → **Privacy & Security** → **Screen Recording**
2. **Enable DeskPad** by checking the box next to it
3. **If DeskPad appears but isn't working:**
   - Uncheck the DeskPad option
   - Check it again to re-enable
4. **Restart DeskPad** for changes to take effect

## Original license notice

```text
MIT License

Copyright (c) 2022 Bastian Andelefski

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

