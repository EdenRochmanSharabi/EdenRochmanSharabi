# Hi, I'm Eden

Developer based in Europe, Madrid and Amsterdam.

## Open Source Contributions

### [scikit-learn](https://github.com/scikit-learn/scikit-learn) — machine learning library for Python

- **HuberRegressor convergence handling** — Fixed incorrect `ValueError` when L-BFGS-B solver fails to converge ([#27777](https://github.com/scikit-learn/scikit-learn/issues/27777)). Now emits `ConvergenceWarning` consistent with other estimators like `LogisticRegression`.
- **f_regression floating-point fix** — Fixed `RuntimeWarning` from negative variance in `r_regression` when features are constant ([#11395](https://github.com/scikit-learn/scikit-learn/issues/11395)). Clamped intermediate squared norms to zero before taking the square root.
- **reconstruct_from_patches_2d** — Fixed incorrect image reconstruction when patch dimensions equal image dimensions ([#10910](https://github.com/scikit-learn/scikit-learn/issues/10910)). The overlap counting formula was missing a constraint on the number of patches.

### [AeroSpace](https://github.com/nikitabobko/AeroSpace) — macOS tiling window manager

- **Native tab detection** — Fixed a long-standing bug ([#68](https://github.com/nikitabobko/AeroSpace/issues/68)) where macOS native tabs were treated as separate windows, causing incorrect tiling. Uses `CGWindowListCopyWindowInfo` (public API) to detect inactive tabs without relying on private APIs.
- **Focus follows mouse** — Implemented `focus-follows-mouse` config option ([#12](https://github.com/nikitabobko/AeroSpace/issues/12)) with debounced mouse tracking and automatic window focus.
- **Sticky floating windows** — Implemented the `sticky` command ([#2](https://github.com/nikitabobko/AeroSpace/issues/2)) allowing floating windows to persist across workspace switches.
