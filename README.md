## Jason Anderson

Incoming Electrical Engineering student at Stanford ('30). I build systems that have to hold up against something real — a robot on a competition field, an opponent across a table, a dataset that won't cooperate.

### What I'm working on

**[Sage](https://github.com/jranderson6364/sage)** · **[live demo →](https://jranderson6364.github.io/sage/)**

An interactive 3D map of ~5,000 movies that doubles as a recommender. The axes are how a film *feels* — levity, threat, intimacy — not what it's about. I learned them with ridge regression over 1,128 MovieLens tag-genome dimensions plus story and review embeddings, trained on 279 hand-scored films and reported on 104 held out: Spearman .86 / .88 / .76, up from .83 / .81 / .69 for a hand-tuned baseline. Recommendations are a weighted reciprocal-rank fusion of three channels — story embeddings, tag genome, and implicit-ALS audience factors. Everything is precomputed in Python and shipped as static JSON to a three.js front end, so there's no backend to run.

**[PkmnTCGAI](https://github.com/jranderson6364/PkmnTCGAI)**

A competitive Pokémon TCG agent for the Kaggle × The Pokémon Company × HEROZ × Matsuo Institute AI Battle Challenge. A heuristic agent is on the ladder now; a self-play, search-trained version is in progress. Every version change is gated by a self-play A/B harness with Wilson 95% confidence intervals, so "better" means measured rather than assumed.

**FRC 5531 Orange Crush** — software lead, 2023–2026

Sole programmer for two years, then began teaching and mentoring other programmers. Closed-loop control in Java/WPILib for a turret, hood, and flywheel shooter; a vision pipeline fusing Limelight MegaTag2 pose estimates into the swerve drivetrain's pose estimator, including the trigonometry to correct for a camera riding a continuously rotating turret; a ballistics model fitting polynomial curves to live calibration data (R²-checked, unit-tested) to turn shot distance into actuator setpoints; and a centralized state machine so six subsystems couldn't fight each other.

### Tools I reach for

Python · Java · NumPy / pandas / scikit-learn · sentence-transformers · three.js · Git

📫 jander6364@gmail.com · [LinkedIn](https://www.linkedin.com/in/jander6364/)
