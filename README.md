# Hi, it's Eden

Developer based in Europe, working in the areas of Valencia and Amsterdam.

I enjoy a wide range of topics, including mathematics, AI/ML, theoretical concepts, especially in mathematics and computer science, UAS, among others. I studied AI & Data Science at Maastricht University, Unmanned Aircraft Systems and Associated Technologies at Univeristy of Valencia and Actuarial Science and Mathematical Finance at the University of Amsterdam (incomplete), and Sociology at the University of Granada.

Outside of formal coursework, I independently study topics that extend or complement my degrees. Recent subjects include category theory, measure theory, and information theory.

I also enjoy lifting heavy weights, rock climbing, running half marathons, diving, long-distance swimming, and generally engaging in hard (physical) activities.


## Open Source Contributions

### [OpenMC](https://github.com/openmc-dev/openmc): Monte Carlo particle transport simulation

- **SphericalMesh.get_indices_at_coords**: Implemented coordinate-to-index lookup for spherical meshes, converting Cartesian `(x, y, z)` to spherical coordinates and returning `(r, θ, φ)` bin indices ([#3867](https://github.com/openmc-dev/openmc/issues/3867), [PR #3919](https://github.com/openmc-dev/openmc/pull/3919)).
- **Model.description property**: Added a `description` attribute to `Model` that serializes as a `<description>` element in the model XML, with round-trip support and automatic omission when empty ([#3586](https://github.com/openmc-dev/openmc/issues/3586), [PR #3956](https://github.com/openmc-dev/openmc/pull/3956)).
- **Material.get_activity chain parameter**: Added an optional `chain` parameter to `Material.get_activity()` and `Results.get_activity()` that accepts a depletion chain for half-life values, falling back to the default ENDF/B-VIII.0 data for nuclides not in the chain ([#3529](https://github.com/openmc-dev/openmc/issues/3529), [PR #3957](https://github.com/openmc-dev/openmc/pull/3957)).
- **Collision count in particle splitting**: Fixed `CollisionFilter` producing biased tallies when weight windows are active by preserving `n_collision` across `Particle::split()` instead of resetting to zero ([#3916](https://github.com/openmc-dev/openmc/issues/3916), [PR #3958](https://github.com/openmc-dev/openmc/pull/3958)).

### [scikit-learn](https://github.com/scikit-learn/scikit-learn): core Python ML library

- **reconstruct_from_patches_2d**: Fixed incorrect image reconstruction when patch dimensions equal image dimensions ([#10910](https://github.com/scikit-learn/scikit-learn/issues/10910), [PR #33643](https://github.com/scikit-learn/scikit-learn/pull/33643)). The overlap counting formula was missing a constraint on the number of patches.
- **DecisionBoundaryDisplay in SVM example**: Replaced manual contour plotting with `DecisionBoundaryDisplay.from_estimator()` in the SVM margins example ([#33980](https://github.com/scikit-learn/scikit-learn/issues/33980), [PR #34192](https://github.com/scikit-learn/scikit-learn/pull/34192)), improving consistency with the modern scikit-learn API.

### [scipy](https://github.com/scipy/scipy): fundamental algorithms for scientific computing

- **lfilter early return on empty input**: Added an early return path to `scipy.signal.lfilter` for zero-length input arrays, returning immediately with the unchanged initial conditions instead of passing empty data through the filter loop ([PR #25334](https://github.com/scipy/scipy/pull/25334)).

### [statsmodels](https://github.com/statsmodels/statsmodels): statistical models and econometrics in Python

- **L-BFGS-B optimizer respects `disp=False`**: Fixed the optimizer printing convergence output unconditionally by passing the `disp` flag through to `scipy.optimize.minimize` ([PR #9823](https://github.com/statsmodels/statsmodels/pull/9823)).
- **Remove dead `cov_p` assignment in GLM fit**: Removed a redundant assignment to `cov_p` that was always overwritten by the hessian-based computation immediately after ([PR #9826](https://github.com/statsmodels/statsmodels/pull/9826)).
- **plot_forest pass `ax` to `dot_plot`**: Fixed `CombineResults.plot_forest` ignoring the caller's `ax` parameter, which created a new figure instead of reusing the provided axes ([#8718](https://github.com/statsmodels/statsmodels/issues/8718), [PR #9829](https://github.com/statsmodels/statsmodels/pull/9829)).
- **Fix GLMInfluence.hat_matrix_diag method name**: Fixed a typo calling `get_hat_matrix()` instead of `get_hat_matrix_diag()`, which raised `AttributeError` when constructing `GLMInfluence` directly ([#9415](https://github.com/statsmodels/statsmodels/issues/9415), [PR #9830](https://github.com/statsmodels/statsmodels/pull/9830)).

## Research

### [The Art of Open Source](https://github.com/EdenRochmanSharabi/The-Art-of-Open-Source): time-series analysis of 4M Pull Requests

A study of 4,048,297 Pull Requests across 580 top open-source repositories (2016-2026). Covers contribution volume trends, temporal patterns, PR response times, contributor retention, the impact of AI coding tools via unsupervised changepoint detection, a composite project health index, and early warning signals for project decline. Data collected via the GitHub GraphQL API, analyzed with time-series decomposition, survival analysis, and forecasting models.

## Projects

### [ScreenFind](https://github.com/EdenRochmanSharabi/ScreenFind): Universal Ctrl+F for macOS

A menu bar app that captures all screens, runs OCR via Apple Vision framework, and highlights matching text in-place with a dimmed overlay. Real-time search, multi-monitor support, off-screen text detection via Accessibility API. Zero third-party dependencies.

### CrossPoint MathML for Xteink X4

Three-repo project to bring mathematical notation to the Xteink X4 e-reader. A [firmware fork](https://github.com/EdenRochmanSharabi/crosspoint-reader) adds on-device MathML linearization to the CrossPoint reader firmware, rendering formulas from plain MathML elements without external dependencies. A [QEMU-based emulator](https://github.com/EdenRochmanSharabi/crosspoint-simulator) runs the real firmware binary on an emulated ESP32-C3 for testing without hardware. A [CLI pipeline](https://github.com/EdenRochmanSharabi/math-epub-pipeline) audits and adapts math EPUBs for the device: TeX-to-MathML conversion, XML repair, font coverage checks, and OCR-based PDF-to-EPUB with verification.
