# Image Filtering and Restoration

Python notebook investigating frequency-domain filtering, image denoising, motion-blur restoration, and the performance of spatial versus frequency-domain Gaussian filtering.

## What the notebook covers

- **Halftone suppression:** Fourier-spectrum analysis with low-pass and notch filtering to reduce periodic dot patterns.
- **Noise reduction:** estimates noise variance and compares adaptive local filtering with bilateral filtering, discussing edge preservation and smoothing.
- **Motion deblurring:** uses a supplied blur kernel to compare inverse filtering and Wiener filtering.
- **Gaussian filtering implementations:** `filter_gauss` in the spatial domain and `filter_gaus_freq` in the frequency domain, with matching edge extension.
- **Performance experiments:** compares filter outputs and execution times for different filter dimensions.

## Getting started

Requires Python 3, JupyterLab, NumPy, SciPy, Matplotlib, and scikit-image.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy scipy matplotlib scikit-image
jupyter lab
```

Open [domaci2_20_662.ipynb](domaci2_20_662.ipynb) and run the cells in order from the repository directory.

## Input data

The original assignment images are **not included in this repository**. To rerun the experiments, supply the following files at the paths expected by the notebook:

- `sekvence/girl_ht.tif`
- `sekvence/lena_noise.tif`
- `sekvence/etf_blur.tif`
- `sekvence/kernel.tif`
- `sekvence/lena.tif`

The notebook contains saved figures and outputs that can be viewed without rerunning it. The notebook text and comments are primarily in Serbian.

## Project context

Academic image-processing coursework (DOS), with implementations, parameter experiments, visual comparisons, and discussion. This repository preserves the original notebook; it is not a packaged library. Dependencies are not version-pinned, and compatibility with current releases has not been verified. Full execution requires the missing input images.

## Reading the results

Saved plots illustrate the tradeoffs between noise suppression and detail preservation, sensitivity of deblurring to regularization, and how filter size affects the relative runtime of spatial and frequency-domain filtering. Timing results depend on the machine and implementation.
