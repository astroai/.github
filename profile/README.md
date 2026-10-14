# astroai

Code, models, and runtime tooling for machine learning on astronomical data. 

We focus on practical bottlenecks in survey science and astrophysics: reading FITS data directly into GPU tensors without NumPy-to-PyTorch glue, computing pixel-level weight and variance maps, quantifying model uncertainties properly, and running reproducible, multi-node workflows on the [CANFAR Science Platform](https://www.canfar.net/).

---

### Core Libraries, FITS I/O & Processing

* **[torchfits](https://github.com/astroai/torchfits)** ([docs](https://astroai.github.io/torchfits)) — High-performance, PyTorch-native FITS I/O powered by a multi-threaded C++ engine with vendored CFITSIO. Reads and writes images, compressed HDUs, and tables directly as tensors, with built-in dataset loaders (`FitsTableIterableDataset`, `FitsCutoutDataset`) for streaming large catalogs and cutouts into training loops.
* **[weightmask](https://github.com/astroai/weightmask)** — Fast generation of per-pixel weight, mask, inverse-variance, and sky maps for astronomical FITS images.
* **[torchregress](https://github.com/astroai/torchregress)** — PyTorch library for regression, uncertainty quantification, and robust estimation.
* **[torchregress-harness](https://github.com/astroai/torchregress-harness)** — External-software benchmarking suite for `torchregress`.

### CANFAR Science Platform & Workbench

* **[canfar-lab](https://github.com/astroai/canfar-lab)** — In-session workbench CLI (`astroai`) for the CANFAR Science Platform. Manages reproducible project environments (`pixi`/`uv` lockfile snapshots on `/arc`), autoscaling distributed Ray clusters, and coding agent setups from a single interface.
* **[canfar-containers](https://github.com/astroai/canfar-containers)** — Lean, pre-configured session images (`images.canfar.net/astroai/*`) for astronomy and ML development on CANFAR.
* **[canfar-skills](https://github.com/astroai/canfar-skills)** — Agent skills and automated scientific workflows tuned for the CANFAR ecosystem.

### Survey Models & Representation Learning

* **[ssl-unions](https://github.com/astroai/ssl-unions)** — Self-supervised representation learning and similarity search for galaxies in the UNIONS survey.
* **[starnet](https://github.com/astroai/starnet)** — Convolutional neural networks and notebooks for extracting stellar parameters and features from spectra (e.g., SDSS APOGEE).

---
There are many updates to come, stay tuned!
