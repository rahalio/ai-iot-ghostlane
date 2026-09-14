# GhostLane — User stories

**Product:** [PRODUCT.md](./PRODUCT.md)


### Perception engineer

- As a perception engineer, I want anticipated tracks when a VRU broadcast drops for N frames, so that the planner is not surprised when the packet returns.
- As a perception engineer, I want shift-noise correction when GPS-reported positions jitter, so that we do not create ghost collisions.
- As a perception engineer, I want a lightweight model profile for the vehicle ECU, so that we do not burn the GPU budget reserved for vision.

### Motion planner

- As a planner, I want uncertainty envelopes on anticipated objects, so that I can modulate speed instead of treating all tracks as truth.
- As a planner, I want an explicit “IoT perception degraded” flag, so that behavior rules can switch to conservative mode.

### Fleet safety operator

- As a safety operator, I want incidents replayable with miss/latency timelines, so that we can separate RF faults from model faults.
- As a safety operator, I want alerts when anticipation confidence stays low on a recurring intersection, so that we can demand infrastructure fixes.

### Network / RF engineer

- As an RF engineer, I want packet-loss and latency histograms joined to GhostLane reliance metrics, so that I know which corridors to remediate.
- As an RF engineer, I want to simulate higher loss on a route in staging, so that we validate fail-safe behavior before rollout.

### Platform administrator

- As a platform admin, I want model versions pinned per vehicle class, so that a robot and a highway AV do not silently share an unfit profile.
- As a platform admin, I want fusion policy templates (IoT-primary at blind intersections vs lidar-primary on open highway), so that sites behave consistently.
