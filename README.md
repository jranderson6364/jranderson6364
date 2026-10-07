## Jason Anderson

Electrical Engineering student at Stanford ('30).

<p>
  <a href="mailto:jander6364@gmail.com"><img src="https://img.shields.io/badge/Email-2B2B2B?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/jander6364/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
</p>

### FRC 5531 Orange Crush — software lead, 2023–2026

Three years on the team. I owned the entire 2026 robot codebase: a 200 Hz control loop across ten subsystems and six operating modes, arbitrated by a central state machine so nothing could issue conflicting commands. Java, WPILib, CTRE Phoenix 6, PhotonVision, PathPlanner.

The parts I'd want to talk about:

- **Sole programmer for two years.** Control, vision, autonomy, and driver tooling were all mine to build and all mine to debug the night before a competition. In my last season I trained the programmers who replaced me.
- **Shooting while driving.** The turret leads the target by projected flight time and corrects for the lag of a turret PID chasing a rotating chassis.
- **A shooting model fit from data, not physics.** Projectile equations don't survive a real game piece, so I drove to known distances, hand-tuned hood angle and flywheel RPM until shots scored, and fit a quadratic through the points. Range in, setpoints out, with R² published live so a bad fit shows up as a number before it shows up as a miss.
- **A turret that can't spin all the way around.** Cable routing leaves a 49° arc the turret cannot cross. Instead of dropping the shot, the code clamps to the nearest limit and feeds a rotation command to the drivetrain, turning the robot itself until the target is back in range.
- **Trusting vision without being fooled by it.** Two PhotonVision coprocessors feed AprilTag pose estimates into the drivetrain's Kalman filter. Bad measurements are rejected on seven conditions; survivors are weighted by distance to the nearest tag. The camera rides the turret, so its pose is recomputed every loop.
- **Tooling.** SysId characterization for feedforward constants, ~40 telemetry channels logged for post-match review, and a manual mode that drives any mechanism live from NetworkTables.

*(Team repo is private. Happy to walk through the code.)*

### [PkmnTCGAI](https://github.com/jranderson6364/PkmnTCGAI)

A competitive Pokémon TCG agent for the Kaggle competition run by The Pokémon Company, HEROZ, and the Matsuo Institute. A heuristic agent is on the ladder; a self-play, search-trained version is in progress. Nothing ships until it beats the previous version in an A/B harness with Wilson 95% confidence intervals.

### [Sage](https://github.com/jranderson6364/sage) · [live demo](https://jranderson6364.github.io/sage/)

A side project: ~5,000 films in a 3D space whose axes are how a movie feels rather than what it's about, doubling as a recommender. Learned axes (ridge regression over tag-genome and embedding features) and a three-channel reciprocal-rank fusion, precomputed in Python and served as static JSON to a three.js front end.

### Right now

- Pushing the self-play agent for **PkmnTCGAI** before the ladder locks in August
- Working through Stroustrup's *A Tour of C++*
- Linear algebra ahead of Stanford's Math 51 sequence
- Competitive programming on Codeforces

### Skills

<p><img src="https://skillicons.dev/icons?i=java,python,js,sklearn,threejs,git,raspberrypi" alt="Java, Python, JavaScript, scikit-learn, three.js, Git, Raspberry Pi" /></p>

**Control** — PID · feedforward · motion profiling · state machines · system identification · real-time loops

**Perception** — computer vision · AprilTag pose estimation · sensor fusion

**ML / data** — scikit-learn · NumPy · pandas · regression · embeddings

**Tools** — WPILib · CTRE Phoenix 6 · PhotonVision · PathPlanner · NetworkTables · Git

### Away from a keyboard

Varsity track and cross country, coaching youth track, and street photography around Detroit.
