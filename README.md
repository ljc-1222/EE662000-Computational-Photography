# EE662000 Computational Photography

## Course Information

- **Course:** EE662000 Computational Photography
- **Language / environment:** Python notebooks
- **Repository scope:** homework code, assignment handouts, local datasets, reference outputs, experiment results, and lecture slides.

This repository collects the coursework notebooks for EE662000 Computational Photography. The notebooks were adjusted to use the local repository layout instead of Google Drive paths.

## Repository Layout

| Path | Topic | Main files |
| --- | --- | --- |
| `hw01/` | HDR imaging: response estimation, radiance construction, white balance, global/local tone mapping, and artifact experiments. | `code/HDR_functions.ipynb`, `code/test_HDR_functions.ipynb`, `code/HDR_flow.ipynb` |
| `hw02/` | Image deblurring: Wiener, Richardson-Lucy, bilateral regularized RL, and total variation methods. | `code/deblur_functions.ipynb`, `code/TV_functions.ipynb`, `code/test_deblur_functions.ipynb` |
| `hw03/` | Super-resolution: interpolation baseline, optimization-based single/multi-image SR, and CNN-based SR training/inference. | `optimization-based/*.ipynb`, `convnet-based/*.ipynb` |
| `slides/` | Lecture slides. | `L*.pdf` |

## Data and Outputs

- Homework input data and golden/reference files are kept inside each homework folder.
- `hw01/Result/`, `hw01/MyHDR_result/`, `hw02/result/`, `hw02/MyDeblur_result/`, `hw03/*/result/`, and `hw03/convnet-based/model_trained/` contain generated outputs or trained checkpoints used by the submitted notebooks.
- Windows `*:Zone.Identifier` files are download metadata only and are ignored by Git.

## Requirements

Use a Python environment with Jupyter support. The current notebooks have been checked with the local conda `base` environment.

Core packages:

```sh
python -m pip install numpy opencv-python matplotlib imageio pillow scipy scikit-image tqdm nbconvert nbformat
python -m pip install proximal torch torchvision
```

Optional CUDA helper functions in `hw02/code/deblur_functions.ipynb` use CuPy:

```sh
python -m pip install cupy-cuda12x
```

## Notes

- The notebooks no longer require Google Drive mounting.
- Keep assignment data files such as `.npy`, images, golden outputs, PDFs, and trained checkpoints when reproducing the submitted results.
