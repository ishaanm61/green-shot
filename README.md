# Real-Time Shot Outcome Prediction from an Instrumented Basketball

**Status: ongoing personal project** (background study complete, hardware prototyping in progress)

An investigation into whether the probability that a basketball shot will score can be estimated *during flight*, using an in-ball inertial sensor and a physics-based model, and shown as a graded "green window" signal rather than a simple make/miss prediction. Rim-mounted sensors provide ground truth so predictions can be tested properly.

## Why

Existing smart balls report metrics such as arc and release time after the shot. This project explores a different question: how early, and how accurately, can the outcome be predicted from the release alone, and can that prediction be well-calibrated?

## Research questions

1. How accurately can release speed, angle and spin be estimated from an in-ball IMU?
2. How well-calibrated is a physics-based make probability compared with a simple baseline?
3. Can the estimate be produced within a latency budget useful for live feedback?

## What's in this repo

| Path | Contents |
|---|---|
| `main.tex` | Source of the background study and project plan |
| `references.bib` | Bibliography |
| `figures/` | Diagrams and plots |
| `[main.pdf]` | Compiled paper |

The paper covers the projectile and rim-entry geometry, the effects of spin and drag, a survey of existing work, sensor requirements, the proposed approach, an evaluation plan, risks, and a timeline.

## Planned approach

IMU in ball -> release detection -> estimate of release speed, angle and spin -> trajectory and probability model -> output signal, with rim sensor outcomes used to evaluate calibration (Brier score, reliability diagrams).

## Progress

- [x] Background theory and literature/patent survey
- [x] Sensor requirements and evaluation plan
- [ ] Rim sensor and data logging
- [ ] Padded-rig IMU prototype
- [ ] Offline make-probability model
- [ ] Real-time implementation
- [ ] In-ball integration and evaluation


## Building the paper

- **Overleaf:** upload the repo as a zip and compile with pdfLaTeX (biber runs automatically).
- **Locally:** `latexmk -pdf main.tex`

## Author

Ishaan Makwana, MEng Computer Engineering, University of Southampton

irm1g26@soton.ac.uk

## Notes

Existing products and patents are described in the paper for context; this project is independent and not affiliated with any of them. Any data collected from other people will be used with their consent.
