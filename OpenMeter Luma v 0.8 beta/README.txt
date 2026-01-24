OpenMeter Luma v 0.8 Beta

This is a beta release of OpenMeter Luma, a real-time waveform visualizer with camera integration.

System Requirements:
- macOS 10.13 or later
- Microphone access (for audio input)
- Camera access (optional, for background video)

Contents:
- OpenmeterLuma.app - Standalone application
- OpenmeterLuma.vst3 - VST3 plugin (for Ableton Live and other DAWs)

═══════════════════════════════════════════════════════════════
HOW IT WORKS
═══════════════════════════════════════════════════════════════

STANDALONE APP:
The standalone app is a self-contained application that:
• Captures audio directly from your Mac's microphone or audio input device
• Displays real-time waveform visualization in its own window
• Works independently - no DAW required
• Perfect for live performances, streaming, or quick visualization

<img src="LUMA STANDALONE.png" width="800" alt="Standalone Application Interface">

How it works:
1. App launches and requests microphone permission
2. You select an audio input device (mic, interface, etc.)
3. Audio is captured via Core Audio (HAL)
4. Waveform is rendered in real-time using OpenGL
5. You can adjust parameters in the settings panel

VST3 PLUGIN:
The VST3 plugin integrates into your DAW (Ableton Live, Logic, etc.):
• Receives audio from the DAW's mixer/arrangement
• Displays waveform for the track it's inserted on
• Can be used on multiple tracks simultaneously
• Each instance shows that track's audio independently
• Supports Ableton Live specific features

<img src="LUMA - VST - CONTROL BOX.png" width="800" alt="VST3 Control Box in Ableton Live">

The control box (shown above) contains all the VST3 settings and parameters when used in Ableton Live. You can adjust waveform appearance, camera settings, and other parameters directly from your DAW.

<img src="LUMA - VST - ABLEON - MULTI CHANNEL.png" width="800" alt="Multi-Channel VST3 Usage in Ableton Live">

Multiple instances can be used simultaneously - one per track. Each instance visualizes that track's audio independently, allowing you to see waveforms for different channels simultaneously.

How it works:
1. Insert plugin on a track in your DAW
2. DAW sends audio to the plugin via VST3 protocol
3. Plugin processes the audio and renders waveform
4. Multiple instances can run at once (one per track)
5. Each instance is independent with its own settings

KEY DIFFERENCES:

Audio Source:
• Standalone: Captures from system audio input (mic/interface)
• VST3: Receives audio from DAW tracks

Use Cases:
• Standalone: Live performance, streaming, quick visualization
• VST3: Music production, mixing, track-specific visualization

Multiple Instances:
• Standalone: One app window, one audio source
• VST3: Multiple plugin instances, one per track

Integration:
• Standalone: Works alone, no DAW needed
• VST3: Integrated into your workflow, follows DAW transport

═══════════════════════════════════════════════════════════════
INSTALLATION
═══════════════════════════════════════════════════════════════

Standalone App:
1. Open the OpenmeterLuma.app
2. Grant microphone permission when prompted
3. Grant camera permission if you want to use camera backgrounds
4. Select your audio input device and click "Enable Audio Input"

VST3 Plugin (for Ableton Live):
1. Copy OpenmeterLuma.vst3 to ~/Library/Audio/Plug-Ins/VST3/
   (or /Library/Audio/Plug-Ins/VST3/ for system-wide installation)
2. Restart your DAW (Ableton Live, etc.)
3. The plugin will appear in your VST3 plugin list
4. Insert it on any track to visualize that track's audio
5. Grant microphone and camera permissions when first used

═══════════════════════════════════════════════════════════════
FEATURES
═══════════════════════════════════════════════════════════════

• Real-time waveform visualization
• Camera background integration

<img src="LUMA CAMARA.png" width="800" alt="Camera Background Integration">

• MIDI support (clock sync, parameter control)
• Customizable waveform parameters (hue, saturation, detail, etc.)
• Multiple rendering modes (stereo split, multiband)
• Ableton Live specific features (when used as VST3 plugin)

Made by Eugene James
