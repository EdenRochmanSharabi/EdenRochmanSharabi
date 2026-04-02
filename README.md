# Hi, I'm Eden

Developer based in Europe, Madrid and Amsterdam.

## Projects

### [ScreenFind](https://github.com/EdenRochmanSharabi/ScreenFind) — Universal Ctrl+F for macOS

A menu bar app that captures all screens, runs OCR via Apple Vision framework, and highlights matching text in-place with a dimmed overlay. Real-time search, multi-monitor support, off-screen text detection via Accessibility API. Zero third-party dependencies.

## Open Source Contributions

### [scikit-learn](https://github.com/scikit-learn/scikit-learn) — core Python ML library

- **HuberRegressor convergence handling** — Fixed incorrect `ValueError` when L-BFGS-B solver fails to converge ([#27777](https://github.com/scikit-learn/scikit-learn/issues/27777)). Now emits `ConvergenceWarning` consistent with other estimators like `LogisticRegression`.
- **reconstruct_from_patches_2d** — Fixed incorrect image reconstruction when patch dimensions equal image dimensions ([#10910](https://github.com/scikit-learn/scikit-learn/issues/10910)). The overlap counting formula was missing a constraint on the number of patches.

### [Qlib](https://github.com/microsoft/qlib) — Microsoft's AI-oriented quantitative investment platform

- **TanhProcess MultiIndex level** — Fixed data preprocessor applying tanh denoising to label columns instead of feature columns due to wrong MultiIndex level lookup ([#1687](https://github.com/microsoft/qlib/issues/1687)).
- **TCN model single-sample batch** — Fixed Temporal Convolutional Network predict crash when the last DataLoader batch contains a single sample, producing a 0-d array incompatible with `np.concatenate` ([#1752](https://github.com/microsoft/qlib/issues/1752)).
- **Workflow datetime level resolution** — Fixed `PortAnaRecord` failing with ambiguous datetime level in MultiIndex by using positional lookup instead of string-based resolution ([#1909](https://github.com/microsoft/qlib/issues/1909)).

### [Hummingbot](https://github.com/hummingbot/hummingbot) — open-source crypto market making and arbitrage engine

- **RESTResponse JSON parsing** — Hardened the REST client to gracefully handle non-JSON responses across all content types, preventing crashes on exchanges that return raw text like `pong` ([#7929](https://github.com/hummingbot/hummingbot/issues/7929)).
- **Backtesting PnL calculation** — Fixed the position executor simulator to use the configured entry price instead of the first candle's close, and corrected the cumulative PnL formula ([#8142](https://github.com/hummingbot/hummingbot/issues/8142)).
- **Backtesting candles connector** — Fixed the backtesting engine to use `candles_connector` when it differs from the trading connector, preventing `UnsupportedConnectorException` on exchanges without candle providers ([#7886](https://github.com/hummingbot/hummingbot/issues/7886)).

### [Dagster](https://github.com/dagster-io/dagster) — Python data orchestration framework

- **Cross-partition automation conditions** — Fixed `will_be_requested()` returning incorrect results when an unpartitioned asset depends on a partitioned one ([#32935](https://github.com/dagster-io/dagster/issues/32935)). Reordered partition boundary checks in `executable_in_same_run()`.

### [Pydantic](https://github.com/pydantic/pydantic) — Python data validation library

- **JSON schema generation with PydanticOmit** — Fixed crash in `model_json_schema()` when a type raising `PydanticOmit` is referenced in multiple fields ([#12706](https://github.com/pydantic/pydantic/issues/12706)). Added omitted definition tracking mirroring the existing `PydanticInvalidForJsonSchema` pattern.

### [AeroSpace](https://github.com/nikitabobko/AeroSpace) — macOS tiling window manager in Swift

- **Native tab detection** — Fixed a long-standing bug ([#68](https://github.com/nikitabobko/AeroSpace/issues/68)) where macOS native tabs were treated as separate windows, causing incorrect tiling. Uses `CGWindowListCopyWindowInfo` (public API) to detect inactive tabs without relying on private APIs.
- **Focus follows mouse** — Implemented `focus-follows-mouse` config option ([#12](https://github.com/nikitabobko/AeroSpace/issues/12)) with debounced mouse tracking and automatic window focus.
- **Sticky floating windows** — Implemented the `sticky` command ([#2](https://github.com/nikitabobko/AeroSpace/issues/2)) allowing floating windows to persist across workspace switches.
