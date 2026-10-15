# astroai

Code, models, and runtime tooling for machine learning on astronomical data. 

We focus on practical bottlenecks in survey science and astrophysics: reading astro data directly into GPU tensors, differentiable data-driven sky modelling, computing pixel-level weight maps, quantifying model uncertainties properly, and running reproducible, multi-node agentic workflows on the [CANFAR Science Platform](https://www.canfar.net/).

---

### Core Libraries, FITS I/O & Processing

* **[torchfits](https://github.com/astroai/torchfits)** ([docs](https://astroai.github.io/torchfits)) — High-performance, PyTorch-native FITS I/O powered by a multi-threaded C++ engine. Reads and writes images, compressed HDUs, and tables directly as tensors, arrow compatibility, with built-in dataset loaders, ready for streaming large catalogs and cutouts into training loops.
* **torchsky** — Torch-native astronomy stack for survey-scale coordinates, spherical geometry, catalog indexing, mapmaking, and joint modelling of sky observations.
* **torchsky-harness** — Scientific validation, upstream parity, benchmarks, and real-data comparisons for torchsky.
* **[xmatcher](https://github.com/astroai/xmatcher)** — Catalogue crossmatching from local sky regions to distributed full-sky matching.
* **[weightmask](https://github.com/astroai/weightmask)** — Fast generation of per-pixel weight, mask (cosmics, streaks, saturation, bad pixels), inverse-variance maps for astronomical images.
* **[torchregress](https://github.com/astroai/torchregress)** — PyTorch library for regression, uncertainty quantification, especially suited for real, difficult regression problems. Not specific to astro data!
* **[torchregress-harness](https://github.com/astroai/torchregress-harness)** — External-software benchmarking suite for `torchregress`.

### CANFAR Science Platform & Workbench

* **[canfar-lab](https://github.com/astroai/canfar-lab)** — In-session workbench CLI for the CANFAR Science Platform. Manages reproducible project environments, resume/save work, autoscaling distributed Ray clusters, and coding agent setups from a single interface.
* **[canfar-containers](https://github.com/astroai/canfar-containers)** — Lean, pre-configured session images (`images.canfar.net/astroai/*`) for astronomy and ML development on CANFAR.
* **[canfar-skills](https://github.com/astroai/canfar-skills)** — Agent skills and automated scientific workflows tuned for the CANFAR ecosystem (Now integrated into the [canfar python client](https://github.com/opencadc/canfar/tree/main/skills/canfar))

### Survey Models & Representation Learning

* **[ssl-unions](https://github.com/astroai/ssl-unions)** — Self-supervised representation learning and similarity search for galaxies in the UNIONS survey.
* **[starnet](https://github.com/astroai/starnet)** — Convolutional neural networks and notebooks for extracting stellar parameters and features from spectra (e.g., SDSS APOGEE).

---
There are many updates to come, stay tuned!
