# LUMA

Waveform visuals for Ableton Live, built to live inside your session instead of sitting off to the side as another utility meter.

`Ableton Live 11/12` | `VST3 Beta` | [![Download latest beta](https://img.shields.io/github/v/release/OpenMeterStudio/LUMA?label=latest%20beta)](https://github.com/OpenMeterStudio/LUMA/releases/latest) | [![Preview](https://img.shields.io/badge/preview-available-blue)](#preview) | [![Features](https://img.shields.io/badge/features-LUMA-blue)](#features) | [![macOS](https://img.shields.io/badge/macOS-install-blue)](#macos) | [![Windows](https://img.shields.io/badge/Windows-install-lightgrey)](#windows) | [![Standalone](https://img.shields.io/badge/standalone-app-blue)](#standalone-app) | [![Feedback](https://img.shields.io/badge/feedback-issues-blue)](https://github.com/OpenMeterStudio/LUMA/issues) | [![Privacy](https://img.shields.io/badge/privacy-beta%20terms-lightgrey)](#privacy--beta) | [![Email](https://img.shields.io/badge/contact-jay@openmeter.studio-yellow)](mailto:jay@openmeter.studio)

LUMA turns your audio into smooth, real-time waveform visuals that live in your DAW or run as their own window. Its not a loudness meter or a spectrum analyzer — its a visual layer for your music that you can use in production, streaming, content creation, or live performance.

The plugin passes audio through untouched. Everything it does is visual.

---

# Preview

| Multi-layer view | Image background + layers |
| --- | --- |
| [![LUMA multi-layer view](<docs/assets/multi layer.png>)](<docs/assets/multi layer.png>) | [![LUMA image background plus multi layers](<docs/assets/IMAGE BACKGROUND PLUS MULTI LAYERS.png>)](<docs/assets/IMAGE BACKGROUND PLUS MULTI LAYERS.png>) |

| Control UI | Stereo split |
| --- | --- |
| [![LUMA control UI](<docs/assets/CONTROL UI.png>)](<docs/assets/CONTROL UI.png>) | [![LUMA stereo split mode](<docs/assets/STEREO SPLIT.png>)](<docs/assets/STEREO SPLIT.png>) |

---

# Why LUMA

Traditional meters tell you how loud your music is. LUMA shows what it feels like.

Drop it on a track or your master bus and your session becomes a customizable, animated waveform display that reacts in real time. Adjust the colors, switch between display modes, layer in a camera feed or an image, and the visuals follow whatever you feed through it.

Run it inside Ableton as a VST3 on individual tracks or the master. Or run the standalone app with any audio input — microphone, interface, loopback — and use it outside a DAW entirely.

Multiple instances in one project layer their waveforms together. Separate out your drums, bass, vocals, and synths across different tracks, and watch the full arrangement scroll by as one composite view.

---

# Features

## Waveform Rendering

GPU-accelerated at 60+ FPS. The waveform follows your audio sample-by-sample through a lock-free ring buffer — no dropped frames, no audio processing, just visuals.

## Display Modes

- **Standard** — classic filled waveform with outline
- **Stereo Split** — separate left and right lanes
- **Multiband** — five frequency bands (sub, low-mid, mid, high-mid, high) each with its own color, in layered or stacked layout
- **Multi-Instance** — waveforms from multiple LUMA instances stacked vertically in one view

## Backgrounds

- **Solid** — adjustable brightness and transparency
- **Camera** — live webcam feed with opacity, hue tint, and audio-reactive shake
- **Image** — any PNG/JPEG loaded as background, with opacity, hue, tint, and scaling

## Visual Controls

Every visual parameter is adjustable and automatable inside Ableton:

- Color maps — HSV, Viridis, Magma, Turbo, with gradient option
- Hue, saturation, fill opacity, outline opacity
- Line width, amplitude scaling
- Show/hide fill and outline independently
- Waveform detail (samples per pixel)
- Camera source, opacity, hue, tint, shake intensity, scale
- Image opacity, hue, tint, size

## Overlays

- **Logo** — clickable `<OpenMeter/>` watermark, toggleable
- **Telemetry** — FPS, view size, samples per pixel, mode, stereo state, camera state, memory, shown on screen

## MIDI

- MIDI clock sync — incoming timing clock drives BPM display
- MIDI learn — map any CC to any visual parameter
- Works in the standalone app (CoreMIDI input)

---

# How to Use It

LUMA fits into a handful of workflows.

**Streaming.** Route your DAW master into LUMA and put it behind your webcam or on a second screen. The standalone app has an always-on-top mode and a compact view that hides the settings panel — it sits over OBS without stealing space.

**Social clips.** Record the standalone app window with your track playing through it. Multiband mode with a camera or image background makes footage that looks better than a generic waveform bounce.

**Video backgrounds.** Feed a microphone into the standalone app through a loopback device. The waveform reacts to speech — subtle motion that syncs to voice without being distracting.

**Studio monitoring.** Put LUMA on a dedicated screen next to your interface. Multiband mode gives you a glanceable reference for what your mix is doing across the frequency spectrum during long sessions.

**Live performance.** Run the standalone app with a MIDI clock input. Map color, amplitude, and mode toggles to MIDI controllers. The waveform changes with the performance.

**Multi-track visualization.** In Ableton, put LUMA on several tracks. The first instance opened becomes the master view and stacks all tracks vertically — kick, bass, vocals, all scrolling in sync.

---

# What You Get

- VST3 plugin for Ableton Live
- Standalone desktop application
- Real-time waveform rendering at 60+ FPS
- Stereo split mode
- Five-band multiband mode
- Image overlay backgrounds
- Live camera backgrounds with audio-reactive shake
- Telemetry overlay
- MIDI clock sync and MIDI learn
- Multi-instance rendering
- Parametric control of every visual aspect
- 4 color map options with gradient coloring

---

# Requirements

- Ableton Live 11 or 12 (for VST3 use)
- VST3 plugin support enabled

### macOS

- macOS 10.13 or later
- Apple Silicon or Intel

### Windows

- Coming soon with the Windows beta release.

---

# Installation

## macOS

### VST3 Plugin

1. Download the latest release.
2. Copy `LUMA.vst3` into:

```
~/Library/Audio/Plug-Ins/VST3/
```

Or install system-wide:

```
/Library/Audio/Plug-Ins/VST3/
```

3. Restart Ableton Live.
4. Go to `Plug-ins → VST3 → LUMA`.
5. Allow microphone permission when prompted (required for audio input routing on macOS).

### Standalone App

1. Download the standalone app from the same release.
2. Move `OpenmeterLuma.app` to your Applications folder.
3. Open it and select an audio input device from the dropdown.
4. Press Space or click Enable to start capture.

If the plugin does not appear in Ableton, verify the `.vst3` bundle is in your VST3 folder and restart Ableton.

---

## Windows

> Windows installation instructions coming soon. The Windows beta is available. Documentation for recommended install locations, troubleshooting, and known issues will be added here.

---

# Standalone App

LUMA also runs as a standalone macOS application that does not require Ableton. It uses the same rendering engine as the VST3 plugin.

- Select any Core Audio input device (built-in mic, audio interface, loopback)
- Adjustable input gain (0x to 2x)
- Tabbed settings panel — Waveform, Images/Video, MIDI, Info
- Detach settings into a separate window or collapse them entirely with Tab
- Always-on-top mode
- Compact mode for full-screen waveform with no UI
- Full keyboard shortcut support
- MIDI learn and MIDI clock sync

---

# First Run

- Play audio through the track (or select an input device in the standalone app).
- Open the LUMA plugin window.
- Experiment with colors, layering, backgrounds, and display modes.
- Keep the plugin window open while using LUMA — rendering only runs while the UI is visible.

---

# Hotkeys

| Key | Action |
| --- | --- |
| `5` | Open image overlay picker |
| `0` | Clear image overlay |
| `9` | Toggle telemetry overlay |
| Click `<OpenMeter/>` | Show or hide logo |

Hotkeys work when the LUMA plugin UI is focused in Ableton, or in the standalone app window.

---

# Beta Testing

Were looking for feedback on:

- Installation and setup
- Performance and frame rate
- Crashes and stability
- Multi-instance behavior
- Visual glitches
- Compatibility with different projects and track layouts
- Feature requests

Run it for 30 to 60 minutes in a normal session and let us know how it goes.

---

# Feedback

Open an issue here:

https://github.com/OpenMeterStudio/LUMA/issues/new

Please include:

- Operating system and version
- Hardware (Apple Silicon, Intel, AMD)
- Ableton version (if applicable)
- Steps to reproduce
- Expected result
- Actual result
- Screenshots or crash logs if available

---

# Roadmap

- Preset management
- Saved MIDI mappings
- Additional visualization modes
- More automation targets
- Performance improvements
- Additional color themes and rendering effects
- Expanded plugin host compatibility

---

# Privacy & Beta

- We only collect information you voluntarily submit through beta feedback.
- Information is used for support, troubleshooting, and product updates.
- We never sell personal information.
- LUMA is beta software. Features and behavior may change between releases.
- Microphone permission is required for audio input on macOS.

---

# Platform Notes

## macOS

- Microphone permission may be required depending on your audio routing. This is a macOS system-level requirement for audio input, not something the app enforces.
- The VST3 plugin renders while its UI is open. Closing the plugin view stops rendering.
- The standalone app runs independently of any DAW.

## Windows

- Documentation will be added as the Windows beta matures.
- Builds are available. Installation and known issues documentation is pending.
