# InspiCrete Terminal Vision

**A cross-platform terminal video player built around full-color ASCII art.**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.jp.md)

![License](https://img.shields.io/badge/License-Not%20Yet%20Selected-lightgrey.svg)
![C++](https://img.shields.io/badge/C%2B%2B-20-00599C.svg?logo=cplusplus)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6.svg?logo=windows)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)

InspiCrete Terminal Vision (ICTV) is an experimental video player written in C++. It aims to convert local video files into full-color ASCII art in real time and render them directly in a terminal window.

Unlike conventional video players that display images as pixels, ICTV uses characters and 24-bit RGB true color to recreate moving images, bringing a lightweight, distinctive, and visually expressive video playback experience to the terminal.

> Turning every frame into a world of characters.

## ✨ Features

- **Full-Color ASCII Video** — Converts video frames into detailed ASCII art with 24-bit RGB true-color support.
- **Real-Time Video Playback** — Decodes and renders frames according to video timestamps for continuous playback.
- **Live Progress Bar** — Displays playback progress, elapsed time, and total video duration at the bottom of the terminal.
- **Frame Rate Monitoring** — Shows both the actual rendering frame rate and the source video's frame rate.
- **Hardware and Runtime Monitoring** — Displays available system information, including CPU usage, memory usage, resolution, decoder, and hardware acceleration status.
- **Native Terminal Experience** — Separates the video output from the bottom status bar for a clean and organized layout.
- **Cross-Platform Design** — Targets Windows, Linux, and macOS.
- **Performance-Oriented Architecture** — Minimizes unnecessary terminal output and memory copies wherever possible.

The project is under active development. Features that have not yet been implemented are planned capabilities and should not be considered available in the current version.

## 🖥️ Preview

*Terminal screenshots coming soon.*

The planned interface uses a vertically divided terminal layout:

```text
┌────────────────────────────────────────────┐
│                                            │
│             Full-Color ASCII Video         │
│                                            │
│        Motion Recreated with Characters    │
│                                            │
├────────────────────────────────────────────┤
│ [========------------] 40%  02:00 / 05:00  │
│ FPS: 28.6 | CPU: 24% | RAM: 62%            │
│ Decoder: FFmpeg | HW Acceleration: Off     │
│ [Space] Pause/Resume          [Q] Quit     │
└────────────────────────────────────────────┘
```

*The layout above is illustrative only. The actual appearance and available information depend on the implementation and the capabilities of the terminal.*

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| C++20 | Core application development |
| CMake | Project configuration and build management |
| FFmpeg | Video container parsing and decoding |
| ANSI/VT Control Sequences | Terminal control and frame rendering |
| 24-bit RGB | Full-color ASCII rendering |
| Catch2 | Unit testing, planned integration |

The project aims to keep dependencies minimal, maintain clear module boundaries, and strike a balance between functionality, performance, and maintainability.

## 🚀 Getting Started

ICTV is currently under development. Build and usage instructions will be refined as the initial implementation and dependency configuration are completed.

### Prerequisites

The planned development environment includes:

- A compiler with C++20 support
- CMake
- Git
- FFmpeg development libraries
- A terminal supporting ANSI/VT control sequences, preferably with 24-bit true-color support

### Build

Once the initial build configuration is complete, the project is expected to be buildable with the following commands:

```bash
git clone https://github.com/yoizuki-hy/InspiCrete-Terminal-Vision
cd InspiCreteTerminalVision

cmake -S . -B build
cmake --build build
```

### Usage

The following command-line interface is planned:

```bash
# Navigate to the build directory
cd ./build

# Display the first frame of a video
./ictv.exe --first-frame "path/test.mp4"

# Play a video
./ictv.exe video.mp4

# Or specify a file path
./ictv.exe "path/test.mkv"

# Play a video using half-block rendering
./ictv.exe --render-mode=half-block "path/test.mp4"

# Display help
./ictv.exe --help

# Display version information
./ictv.exe --version
```

These commands describe the intended command-line interface. They may not work as expected until the corresponding features are implemented.

## ⌨️ Controls

The following playback controls are planned:

| Key | Action |
|---|---|
| `Space` | Pause / Resume playback |
| `Q` | Quit the player |
| `Esc` | Quit the player |
| `A` | Seek backward 5 seconds |
| `D` | Seek forward 5 seconds |

Mouse interaction, click-to-seek functionality, and a draggable progress bar may be considered in future development.

## 🧩 Architecture

ICTV follows a modular design, separating different responsibilities into relatively independent components:

- **CLI** — Handles command-line argument parsing and configuration management.
- **VideoDecoder** — Processes video streams and decodes video frames.
- **AsciiConverter** — Handles character mapping, brightness adjustment, and color conversion.
- **TerminalRenderer** — Manages terminal output, interface layout, and rendering buffers.
- **StatusBar** — Displays playback progress, frame rate, video information, and runtime status.
- **SystemMonitor** — Collects platform-specific system performance metrics.
- **PlaybackController** — Coordinates playback timing, input handling, and interactions between modules.

The goal is to keep the overall design simple and practical while ensuring that individual modules remain testable and maintainable.

## 🗺️ Roadmap

- [x] Establish the C++20 and CMake project structure
- [x] Implement command-line argument parsing and error handling
- [x] Integrate FFmpeg video decoding
- [x] Implement ASCII character conversion and brightness mapping
- [x] Implement 24-bit RGB full-color character rendering
- [x] Implement a real-time status bar anchored to the bottom of the terminal
- [x] Display playback progress and timing information
- [x] Calculate and display the actual rendering frame rate
- [x] Display CPU usage, memory usage, decoder information, and hardware acceleration status when available
- [x] Implement pause, resume, and quit controls
- [x] Support terminal window resizing and safely restore terminal state on exit
- [ ] Validate builds on Windows, Linux, and macOS
- [ ] Optimize rendering performance
- [ ] Explore interactive video seeking and enhanced hardware decoding

## 🤝 Contributing

Suggestions, bug reports, feature requests, and technical discussions are welcome.

When contributing, please follow these principles:

- Prioritize clear, maintainable modern C++ code.
- Preserve cross-platform compatibility wherever possible.
- Avoid unnecessary third-party dependencies.
- Add tests for code changes whenever practical.
- Document platform-specific differences and feature limitations clearly.
- Do not describe unverified functionality as implemented.

Contribution guidelines and development standards will be refined as the project matures.

## 📄 License

The project has not yet selected an open-source license.

A suitable license will be chosen based on the project's needs before official distribution and code reuse are permitted. Until a license is formally added, do not assume that the repository's code is freely available for use, modification, or redistribution.

## 👨‍💻 Author

**InspiCrete Studio**

*Exploring the intersection of software, visual art, and interactive experiences.*

---

*InspiCrete Terminal Vision — Reimagining moving images, one character at a time.*
