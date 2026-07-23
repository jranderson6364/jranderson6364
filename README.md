## Jason Anderson

Incoming Electrical Engineering student at Stanford ('30). I write control software for machines that get one attempt, in front of a crowd, with no chance to redeploy.

### FRC 5531 Orange Crush — software lead, 2023–2026

Three years on the team, two of them as its only programmer. I owned the entire 2026 robot codebase: a 200 Hz control loop across ten subsystems and six operating modes, arbitrated by a central state machine so nothing could issue conflicting commands. Java, WPILib, CTRE Phoenix 6, PhotonVision, PathPlanner.

The parts I'd want to talk about:

- **Shooting while driving.** The turret leads the target by projected flight time and compensates for the lag between a rotating chassis and a turret PID that can't quite keep up.
- **A turret that can't spin all the way around.** Cable routing left a 49° arc the turret physically cannot cross. Rather than give up the shot, the code clamps the turret to its nearest limit and feeds a rotation command into the drivetrain, so the robot turns itself until the target is reachable again.
- **Trusting vision without being fooled by it.** Two PhotonVision coprocessors run AprilTag pose estimation into the drivetrain's Kalman filter. Measurements are rejected on seven conditions (spin rate, latency, off-field poses, two tag-distance gates, single-tag ambiguity, gyro disagreement); survivors are weighted by distance to the nearest tag. The turret camera moves with the turret, so its pose in robot space is recomputed every loop.
- **Failing gracefully.** A debounced stall detector catches an intake drawing duty but not spinning, then bumps the pivot to shake the jam loose. Turret, hood, and flywheel error map to a green/yellow/red readout so the driver never fires before the mechanisms converge.
- **Tooling.** SysId characterization for feedforward constants, a polynomial shooting model fit to measured range data with live R², ~40 telemetry channels logged for post-match review, and a manual mode that drives any mechanism from a NetworkTables browser.

*(Team repo is private. Happy to walk through the code.)*

### [PkmnTCGAI](https://github.com/jranderson6364/PkmnTCGAI)

A competitive Pokémon TCG agent for the Kaggle competition run by The Pokémon Company, HEROZ, and the Matsuo Institute. A heuristic agent is on the ladder; a self-play, search-trained version is in progress. Nothing ships until it beats the previous version in an A/B harness with Wilson 95% confidence intervals.

### [Sage](https://github.com/jranderson6364/sage) · [live demo](https://jranderson6364.github.io/sage/)

A side project: ~5,000 films in a 3D space whose axes are how a movie feels rather than what it's about, doubling as a recommender. Learned axes (ridge regression over tag-genome and embedding features) and a three-channel reciprocal-rank fusion, precomputed in Python and served as static JSON to a three.js front end.

### Tools I reach for

Java · Python · WPILib · PhotonVision · NumPy / pandas / scikit-learn · Git

📫 jander6364@gmail.com · [LinkedIn](https://www.linkedin.com/in/jander6364/) · [LeetCode](https://leetcode.com/u/jander6364/)
