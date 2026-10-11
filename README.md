# InspiCrete Terminal Vision

**A cross-platform terminal video player powered by colorful ASCII art.**

[English](README.md) | [简体中文](README.zh-CN.md) | [日本語](README.jp.md)

![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
![C++](https://img.shields.io/badge/C%2B%2B-20-00599C.svg?logo=cplusplus)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6.svg?logo=windows)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)

InspiCrete Terminal Vision (ICTV) is an experimental C++ video player that transforms local video files into dynamic, full-color ASCII art directly in your terminal.

Instead of displaying pixels on a conventional video canvas, ICTV recreates moving images using characters and 24-bit RGB colors, bringing video playback into the terminal in a lightweight, distinctive, and visually expressive way.

> Turning every frame into a world of characters.

## ✨ Features

- **Colorful ASCII Video** — Transform video frames into detailed character art with 24-bit RGB true color.
- **Real-Time Playback** — Decode and render video frames with timestamp-based playback scheduling.
- **Live Progress Bar** — Display playback progress, elapsed time, and total duration at the bottom of the terminal.
- **FPS Monitoring** — Show actual rendering FPS alongside the source video's frame rate.
- **Hardware & Runtime Status** — Present available CPU, memory, resolution, decoder, and hardware-acceleration information.
- **Terminal-Native Experience** — Keep video output and the status bar in separate terminal regions.
- **Cross-Platform Design** — Target Windows, Linux, and macOS.
- **Performance-Oriented Architecture** — Minimize unnecessary terminal output and memory copying.

Features are being developed incrementally. Items not yet implemented should be treated as planned capabilities rather than guaranteed functionality.

## 🖥️ Preview

*Terminal preview coming soon.*

The intended interface consists of two regions:

```text
┌────────────────────────────────────────────┐
│                                            │
│          COLORFUL ASCII VIDEO              │
│                                            │
│       Characters recreate each frame       │
│                                            │
├────────────────────────────────────────────┤
│ [========------------] 40%  02:00 / 05:00  │
│ FPS: 28.6 | CPU: 24% | RAM: 62%            │
│ Decoder: FFmpeg | HW Accel: OFF            │
│ [Space] Pause/Resume        [Q] Quit       │
└────────────────────────────────────────────┘
```

*Illustrative layout only. Actual appearance and available metrics depend on implementation and terminal capabilities.*

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| C++20 | Core implementation |
| CMake | Build system |
| FFmpeg | Video demuxing and decoding |
| ANSI/VT sequences | Terminal control and rendering |
| 24-bit RGB | Full-color character rendering |
| Catch2 | Unit testing, planned |

The project aims to keep its dependencies focused and its architecture modular.

## 🚀 Getting Started

ICTV is under active development. Build instructions will be finalized once the initial implementation and dependency configuration are ready.

### Prerequisites

The planned development environment includes:

- A C++20-compatible compiler
- CMake
- Git
- FFmpeg development libraries
- A terminal with ANSI/VT support and preferably 24-bit color support

### Build

Once the initial build configuration is available, the intended workflow is:

```bash
git clone <repository-url>
cd InspiCreteTerminalVision

cmake -S . -B build
cmake --build build
```

Replace `<repository-url>` with the actual URL of this repository.

### Usage

The intended command-line interface is:

```bash
ictv video.mp4
ictv "path/to/my video.mkv"

ictv --help
ictv --version
```

The commands above describe the planned interface. They may not work until the corresponding features have been implemented.

## ⌨️ Controls

Planned playback controls:

| Key | Action |
|---|---|
| `Space` | Pause / Resume |
| `Q` | Quit |
| `Esc` | Quit |

Mouse-based seeking and draggable progress bars may be considered for a future release.

## 🧩 Architecture

ICTV is designed around small, focused modules:

- **CLI** — Command-line arguments and configuration.
- **VideoDecoder** — Video stream handling and frame decoding.
- **AsciiConverter** — Character mapping, brightness processing, and color conversion.
- **TerminalRenderer** — Terminal output, layout, and rendering buffers.
- **StatusBar** — Playback progress, FPS, video metadata, and status display.
- **SystemMonitor** — Platform-specific runtime and hardware metrics.
- **PlaybackController** — Playback timing, input handling, and coordination.

The goal is to make each component independently testable while keeping the overall design practical and maintainable.

## 🗺️ Roadmap

- [ ] Establish the C++20 and CMake project structure
- [ ] Implement command-line arguments and error handling
- [ ] Integrate FFmpeg video decoding
- [ ] Implement ASCII conversion and brightness mapping
- [ ] Add 24-bit RGB character rendering
- [ ] Create a persistent bottom status bar
- [ ] Display playback progress and elapsed time
- [ ] Measure and display actual rendering FPS
- [ ] Add CPU, memory, decoder, and acceleration status where available
- [ ] Implement pause, resume, and exit controls
- [ ] Handle terminal resizing and restore terminal state safely
- [ ] Verify builds on Windows, Linux, and macOS
- [ ] Optimize rendering performance
- [ ] Explore interactive seeking and hardware decoding enhancements

## 🤝 Contributing

Contributions, ideas, bug reports, and technical discussions are welcome.

Before submitting a change, please keep the following principles in mind:

- Prefer clear, maintainable C++20 code.
- Preserve cross-platform compatibility.
- Avoid unnecessary dependencies.
- Test changes whenever practical.
- Document platform-specific behavior and limitations.
- Do not claim functionality that has not been verified.

Contribution guidelines may be expanded as the project matures.

## 📄 License

The project license has not yet been selected.

A license will be added before the project is distributed for reuse. Until then, please do not assume that the repository is available under an open-source license.

## 👨‍💻 Author

**InspiCrete Studio**

*Exploring the intersection of software, visuals, and interactive experiences.*

---

*InspiCrete Terminal Vision — video, reimagined in characters.*
