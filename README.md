# LUMA

Waveform visuals for Ableton on macOS, built to live inside the session instead of sitting off to the side as a utility meter.

`macOS only` `Ableton Live 11/12` `VST3 beta`

[Download latest beta](https://github.com/OpenMeterStudio/LUMA/releases/latest) | [Preview](#preview) | [Why LUMA](#why-luma) | [Install](#install) | [Feedback](#feedback) | [Privacy and terms](#privacy-and-beta-terms)

LUMA is for producers and creators who want motion, shape, and track-specific visuals, not just loudness readouts. Put it on a track or the master, dial in the look, and turn your session into something you can actually perform with or capture on screen.

## Preview

| Multi-layer view | Image background + layers |
| --- | --- |
| [![LUMA multi-layer view](<docs/assets/multi layer.png>)](<docs/assets/multi layer.png>) | [![LUMA image background plus multi layers](<docs/assets/IMAGE BACKGROUND PLUS MULTI LAYERS.png>)](<docs/assets/IMAGE BACKGROUND PLUS MULTI LAYERS.png>) |

| Control UI | Stereo split |
| --- | --- |
| [![LUMA control UI](<docs/assets/CONTROL UI.png>)](<docs/assets/CONTROL UI.png>) | [![LUMA stereo split mode](<docs/assets/STEREO SPLIT.png>)](<docs/assets/STEREO SPLIT.png>) |


## What You Get

- A VST3 plugin for Ableton Live on macOS.
- Real-time waveform rendering on any track or the master bus.
- Stereo split, multi-band mode, image backgrounds, overlays, color controls, telemetry overlay, and MIDI sync.
- Multi-instance behavior for stacked or track-by-track visual setups.
- A plugin-first beta today, with a standalone app planned later.

## Requirements

- macOS 10.13 or later
- Ableton Live 11 or 12
- VST3 plugin support enabled in Ableton
- Microphone permission for audio input

## Install

1. Download the latest release.
2. Copy `OpenmeterLuma.vst3` to `~/Library/Audio/Plug-Ins/VST3/`. Use `/Library/Audio/Plug-Ins/VST3/` if you want a system-wide install for all users.
3. Quit and reopen Ableton Live to force a rescan.
4. Open Ableton and go to `Plug-ins` -> `VST3` -> `OpenmeterLuma`.
5. Drop it on a track or the master and allow microphone permission when prompted.

If Ableton does not see it, confirm the bundle exists at `~/Library/Audio/Plug-Ins/VST3/OpenmeterLuma.vst3` and then fully restart Ableton again.

## First Run

- Enable monitoring or play back audio so the plugin has signal.
- Open the plugin UI and adjust waveform style, layering, color, and MIDI sync.
- Leave the UI open while testing so hotkeys and overlays respond.

## Multiple Instances

- The first LUMA instance opened in a project becomes the master renderer.
- Additional instances stay small but still feed their track audio into the master view.
- To change which instance becomes the master, remove all LUMA instances and load the desired track first.
- If the main view disappears, close and reopen the first-loaded instance.

## Hotkeys

| Key | Action |
| --- | --- |
| `5` | Open image overlay picker |
| `0` | Clear image overlay |
| `9` | Toggle telemetry overlay |
| Click `<Openmeter/>` | Show or hide logo |

Hotkeys work when the LUMA plugin UI has focus in Ableton.


## Why LUMA

- Waveform-first visuals instead of basic meter bars, so the motion feels musical and screen-ready.
- Insert it directly on individual tracks or the master to see exactly where energy is coming from in a session.
- Run multiple instances in one project for layered, track-aware visuals instead of a single generic readout.
- Switch between looks like stereo split, multi-band mode, layered views, and image-backed compositions.
- Built for Ableton workflows, so it feels like part of the set or project rather than a detached desktop visualizer.

## Beta Testing Focus

- Confirm the plugin appears reliably after install and rescan.
- Run it for 30 to 60 minutes and watch for stutter, crashes, UI freezes, or dropped frames.
- Test one instance per track if you want stacked multi-channel visuals.
- Switch between simple and busy projects to check stability under different session loads.
- Verify image backgrounds, overlays, and different visual modes if you use those features.

## Feedback

Open an issue here: [GitHub issues](https://github.com/OpenMeterStudio/LUMA/issues/new)

Include:

- macOS version
- Mac type: Apple Silicon or Intel
- Ableton version: 11 or 12
- Steps to reproduce
- Expected result
- Actual result
- Crash message, screenshot, or `OpenmeterLuma.log` if available

## Privacy And Beta Terms

- We collect the contact info and beta feedback you send us.
- We use it for beta access, updates, and troubleshooting.
- We do not sell personal information.
- LUMA is beta software, so features may change and crashes are possible.
- Microphone permission is required for audio input.

This README is the GitHub-safe version of the beta portal, so the privacy and beta terms summary lives here instead of on a separate site.
