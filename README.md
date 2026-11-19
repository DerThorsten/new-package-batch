# New package batch: emscripten-forge in JupyterLite

A [JupyterLite](https://jupyterlite.readthedocs.io) deployment showcasing packages recently added to
[emscripten-forge](https://github.com/emscripten-forge/recipes). Everything runs in your browser with the
[xeus-python](https://github.com/jupyter-xeus/xeus-python) kernel; no server, no install.

**Try it:** https://derthorsten.github.io/new-package-batch/

| notebook | package | what it shows | PR |
|---|---|---|---|
| `landlab.ipynb` | [landlab](https://landlab.csdms.io) | evolve an eroding mountain range (uplift, rivers, hillslopes) | [#8581](https://github.com/emscripten-forge/recipes/pull/8581) |
| `rdkit.ipynb` | [RDKit](https://www.rdkit.org) | molecules rendered inline, descriptors, similarity, substructure search | [#8590](https://github.com/emscripten-forge/recipes/pull/8590) |
| `shap.ipynb` | [SHAP](https://shap.readthedocs.io) | explain a scikit-learn model with beeswarm / waterfall / dependence plots | [#8585](https://github.com/emscripten-forge/recipes/pull/8585) |
| `soundfile.ipynb` | [libsndfile](https://libsndfile.github.io/libsndfile/) + [python-soundfile](https://python-soundfile.readthedocs.io) | synthesize, write, read and play audio; spectrogram | [#8588](https://github.com/emscripten-forge/recipes/pull/8588) |

The kernel environment is defined in [`environment.yml`](environment.yml).

## Build locally

```bash
micromamba create -n build-env -f .github/build-environment.yml
micromamba activate build-env
jupyter lite build --contents content --output-dir dist
jupyter lite serve --output-dir dist
```
