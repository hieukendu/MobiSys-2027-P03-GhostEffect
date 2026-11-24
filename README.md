# GhostEffect

Artifact and manuscript for **GhostEffect: Budgeted Exactly-Once Recovery of GUI-Only Effects for Mobile Agents**.

## Contents

- `artifact/`: stdlib-only Python artifact, generated results, emulator measurements, and PRISM model.
- `manuscript/`: LaTeX source, generated tables/figures, and the compiled manuscript PDF.
- `STATUS.md`: current project status and evidence boundaries.
- `others/notes.md`: reproducibility notes and simulator configuration details.

## Reproduce the artifact

Requirements: Python 3.11+ and a POSIX shell (Linux, macOS, or WSL on Windows).

```sh
./artifact/run_all.sh
./manuscript/build.sh
```

The artifact uses only the Python standard library. Most outputs are seeded and
byte-stable; host timing measurements can vary across machines. The emulator
measurement CSVs under `artifact/results/real/` are read-only inputs to the
measured-parameter simulation.

The repository contains scripted emulator measurements and model-based
simulation. It does not claim an LLM-agent run, VLM evaluation, or physical-phone
measurement; see `STATUS.md` for the current scope and limitations.

## Public-release boundary

This repository intentionally omits the internal review packet, the local
archive containing the original `.git` directory, archive manifests, and raw
campaign logs containing machine-local paths. Those files remain in the original
working directory and are not required to reproduce the checked-in artifact.
