# WhAM Tape Looper

A JUCE-based tape looper frontend for [WhAM (Whale Acoustics Model)](https://github.com/Project-CETI/wham). Records audio, sends it to a Gradio-hosted WhAM backend for whale coda generation, and plays back the result in a loop.

---

## Quick Start (macOS)

### Prerequisites

- **CMake** 3.22+ (`brew install cmake`)
- **Xcode Command Line Tools** (`xcode-select --install`)

### Build & Run

```bash
git clone --branch wham --recursive https://github.com/panditanvita/flowerjuce.git
cd flowerjuce
mkdir build && cd build
cmake ..
cmake --build . --config Release
open "TapeLooper_artefacts/Tape Looper.app"
```

### Usage

1. Select **WhAM** from the startup dialog
2. Enable mic input on a track (click the mic icon so it turns yellow)
3. Arm recording (click **R**)
4. Press **Play** to start recording
5. Press **Play** again to stop and loop
6. Click the whale button to send audio to the model and hear the generated coda

The backend defaults to `https://anvitax-wham.hf.space/`. You can change the Gradio URL in Settings.

---
