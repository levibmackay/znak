# Znak

Real-time sign language recognition for iOS, built with Swift and on-device computer vision.

Znak reads sign language through your phone's camera and identifies signs in real time, using Apple's Vision framework for hand pose detection and a CoreML model for classification. No cloud processing — everything runs on-device.

The name comes from *znak*, the word for "sign" in Serbian, Croatian, and Bosnian.

## Status

🚧 Early development — currently building static sign recognition (starting with the ASL alphabet).

## How it works

1. **Hand tracking** — Apple's Vision framework (`VNDetectHumanHandPoseRequest`) extracts hand joint landmarks from the live camera feed
2. **Classification** — a CoreML model maps landmark positions to signs
3. **Display** — recognized signs are shown in real time as an overlay on the camera view

## Tech stack

- Swift / SwiftUI
- AVFoundation (camera capture)
- Vision framework (hand pose detection)
- CoreML (sign classification)

## Roadmap

- [x] Camera capture + live hand landmark tracking
- [ ] Static sign classification (small starting set)
- [ ] Full ASL alphabet support
- [ ] UI polish — sign reference guide, confidence feedback
- [ ] Dynamic (motion-based) sign recognition

## Setup

Requires Xcode and iOS 17+ (adjust once you confirm your target).

```bash
git clone https://github.com/levibmackay/znak.git
cd znak
open Znak.xcodeproj
```

## License

TBD
