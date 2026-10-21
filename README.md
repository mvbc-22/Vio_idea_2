# Vio_idea_2: Energy-Efficient UAV VIO/SLAM Architectures

## Status

Research concept exploration. No estimator, sensor-fusion algorithm, or
hardware implementation has been selected or implemented. This project is
separate from `Vio_idea_1`, whose asynchronous feature tracker remains frozen.

## Research objective

Investigate whether a UAV visual-inertial odometry or SLAM architecture can
reduce system energy while maintaining a specified level of trajectory
accuracy, robustness, and update rate.

The study will treat energy efficiency as an end-to-end system property. It
will account for sensing, data movement, event/frame representation, feature
processing, state estimation, and compute-platform power rather than assuming
that changing a single algorithmic component guarantees an energy benefit.

## Initial research questions

1. Which parts of a UAV VIO/SLAM pipeline dominate energy under representative
   flight workloads?
2. How do event, frame, and hybrid sensor representations affect energy,
   latency, bandwidth, and trajectory quality when compared fairly?
3. Which state-estimation and update-scheduling strategies provide useful
   accuracy/robustness per joule?
4. Do observed gains persist across motion regimes, lighting conditions,
   datasets, and compute platforms?

These are questions to investigate, not claims that any architecture is
already more efficient or novel.

## Initial workflow

1. **Define scope and metrics.** Specify the UAV operating conditions,
   acceptable trajectory error, required update rate, and energy measurement
   boundary.
2. **Review prior work.** Map event/frame/IMU representations, estimator
   families, scheduling strategies, and published energy measurement methods.
3. **Select reproducible baselines.** Choose established VIO/SLAM systems and
   datasets with suitable ground truth; record versions and configurations.
4. **Establish measurement protocol.** Measure energy or power, latency,
   throughput, bandwidth, and trajectory quality on a declared platform.
5. **Identify one testable architectural change.** Choose it only after the
   literature review and baseline measurements; isolate it with ablations.
6. **Evaluate and report.** Repeat across sequences and operating conditions,
   include uncertainty and failure cases, and avoid unsupported efficiency or
   novelty claims.

## Reproducibility requirements

- Keep source code, experiment configuration, and result-generation scripts
  versioned.
- Record dataset sequence, sensor calibration, software versions, platform,
  power-measurement method, and timing boundary for each run.
- Preserve raw datasets outside Git; document acquisition and checksums where
  appropriate.
- Report accuracy and robustness alongside energy, latency, and throughput.
- Keep the Vio_idea_1 frozen algorithm unchanged unless a separate experiment
  demonstrates that its specification must be revisited.

## Initial project structure

```text
Vio_idea_2/
├── README.md
├── .gitignore
├── docs/       # literature notes and protocol specifications
├── configs/    # versioned experiment configurations
├── src/        # added only after the first experiment is specified
└── results/    # reproducible summaries and plots
```

The directories will be created when the corresponding work begins. This
initial scaffold intentionally contains no implementation or copied tracker
code.
# Vio_idea_2
