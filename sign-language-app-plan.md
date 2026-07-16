# Sign Language Recognition App — Build Plan

**Goal:** Learn Swift, ship a real iOS computer vision app, own every decision in it.
**Rule:** Claude reviews and unblocks. You write the code.

---

## Phase 0 — Swift & SwiftUI Fundamentals
*Goal: comfortable writing basic iOS apps without looking everything up.*

- [ ] Complete Apple's Swift Playgrounds or the official Swift Tutorials
- [ ] Complete a SwiftUI tutorial (Apple's "Landmarks" tutorial is the standard one)
- [ ] Build one throwaway toy app (todo list, counter, whatever) start to finish, alone
- [ ] Understand: `@State`, `@Binding`, basic navigation, and how views update

**Checkpoint:** You can build a simple multi-screen SwiftUI app without a tutorial open.

---

## Phase 1 — Camera & Vision Framework Basics
*Goal: get a live camera feed on screen and pull hand landmarks from it.*

- [ ] Get `AVCaptureSession` working — live camera preview in your app
- [ ] Read Apple's docs on `VNDetectHumanHandPoseRequest`
- [ ] Get hand joint landmarks printing to console from live camera frames
- [ ] Draw the landmarks as an overlay on the camera preview (visual proof it's working)

**Checkpoint:** You can see your own hand's joint points tracked live on screen.

---

## Phase 2 — Static Sign Classification (MVP)
*Goal: recognize a handful of static signs (e.g. ASL alphabet letters) reliably.*

- [ ] Pick a small starting set (5–10 letters/signs, not the full alphabet)
- [ ] Find or build a labeled dataset of hand landmark positions for those signs
- [ ] Train a small classifier (landmarks → sign label) — start simple, e.g. a basic
      neural net or even nearest-neighbor on landmark vectors
- [ ] Convert/import the model with CoreML
- [ ] Wire it into the app: live landmarks → prediction → label shown on screen

**Checkpoint:** App correctly identifies your chosen static signs in real time, most of the time.

---

## Phase 3 — Expand & Improve
*Goal: make it a real product, not a demo.*

- [ ] Expand to the full alphabet (or a meaningful word set)
- [ ] Improve accuracy — more training data, better model, confidence thresholds
- [ ] Add basic UI polish: onboarding, sign reference guide, feedback on misreads
- [ ] Handle edge cases: bad lighting, hand partially out of frame, etc.

**Checkpoint:** Something you'd actually be comfortable demoing in an interview.

---

## Phase 4 — Stretch (Optional)
*Goal: push toward dynamic signs, not just static letters.*

- [ ] Research sequence-based sign recognition (signs that involve motion, not just a pose)
- [ ] Attempt a small set of dynamic word signs using landmark sequences over time

---

## Working with Claude
- Bring specific problems, not "build feature X" — e.g. "my `VNDetectHumanHandPoseRequest`
  callback is crashing on nil" or "how should I structure the landmark buffer for a
  sequence model"
- Use me to review code you've written, explain concepts you hit, and help debug —
  not to generate files
- Loop back in after each checkpoint to sanity-check your approach before moving on

---

## What comes after this
Once this ships, the plan is to reuse what you learn here (Swift, CoreML, on-device
inference) toward the Jarvis-style agent app, then the agent dev tool.
