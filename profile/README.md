# DASH-01

DASH-01 is a 15 kg biped robot built and run by EPFL students. Six CubeMars motors are driven over CAN by a Raspberry Pi 3B. Its policies are trained with reinforcement learning in MuJoCo, then run on the robot at 100 Hz.

## Repositories

| Repo | Role | Status |
| --- | --- | --- |
| [`dash-sim2real`](https://github.com/Dash-organisation/dash-sim2real) | the living codebase: robot stack, training, model of the current robot | active |
| [`dash-reports`](https://github.com/Dash-organisation/dash-reports) | reports and galleries of the RL series, videos, raw logs | active |
| `dash-cad` | all the CAD, exports and files to print | coming later |
| [`DASH-01-archive`](https://github.com/Dash-organisation/DASH-01-archive) | the complete old repo, with its full history | archived, read-only |

## New to the project?

1. `git clone https://github.com/Dash-organisation/dash-sim2real.git`
2. Read its `README.md`: installation, tests, deployment, running a policy.
3. Then read `docs/rl/EXPERIMENTS.md` (what has been tried in RL) and `HISTORY.md` (where the project comes from).
4. Clone `dash-reports` only if you want the videos and reports, and `dash-cad` only for the mechanics.

## Current status (2026-11-23)

- **On the robot.** The standing policy `standing04_xshape_best` runs on the robot at 100 Hz, with every safety check active.
- **Not validated yet: standing.** The policy lets the robot tip forward, because of a gap between the model and the real robot (−6.5° at rest).
- **Next step:** measure that gap, then retrain on a corrected plant.

## Contacts

- Robot, onboard stack, sim-to-real: Tim
- RL training: Léo-Paul (`leorizkallah`)
