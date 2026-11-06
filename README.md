# Exercise 01: Free-space path loss at 7.125-8.4 GHz

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<USER>/<REPO>/blob/main/exercises/01_free_space_path_loss/01_free_space_path_loss.ipynb)

## Goal
Build the first block of a link budget for IMT / 6G coexistence studies in the
7.125-8.4 GHz range: how much power is lost between a transmitter and a receiver,
and how that loss changes with distance and frequency.

## What it covers
- Free-space path loss (FSPL) implemented in NumPy and validated against a
  reference value (92.45 dB at 1 km and 1 GHz).
- FSPL as a function of distance at the band edges and band center.
- Sensitivity comparison: distance vs. frequency.
- A first protection-distance calculation from an I/N criterion.

## Key results
| Observation | Value |
|---|---|
| Loss added by doubling the distance | 6.02 dB |
| Loss added across the whole band (7.125 to 8.4 GHz, at 1 km) | 1.43 dB |
| Free-space protection distance at 7.125 GHz | ~168 km |
| Free-space protection distance at 8.4 GHz | ~142 km |

Distance dominates over frequency by a wide margin inside this band.

## Assumptions and limitations
- The system parameters (EIRP 50 dBm, 0 dBi receiver gain, -94 dBm noise floor,
  I/N = -10 dB) are **illustrative placeholders**, not real system values. They
  will be replaced with sourced parameters in later exercises.
- Free space is the best-case propagation path (no terrain, clutter, antenna
  patterns or atmosphere), so the distances above are a conservative upper
  bound, not a prediction.

## Tools
Python, NumPy, Matplotlib.

## Next
Exercise 02: terrain profile between two points using a digital elevation model.
