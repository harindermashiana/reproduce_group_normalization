# Reproduce Group Normalization — Final Project
Reproduced and evaluated Group Normalization (GN) vs Batch/Layer/Instance Normalization on Tiny ImageNet-200 using a custom TensorFlow model and experimental pipeline. You can find additional details/results/experiments in the PDF present in this repo.

## Why this project matters
- Demonstrates reproducible experimental ML: implementing a research normalization method, integrating it into a model, running controlled comparisons, and visualizing results.
- Shows hands-on experience with TensorFlow custom layers, dataset handling (Tiny ImageNet-200), and experimental analysis.

## Key highlights
- Implemented `GroupNormalization` (custom Keras layer) and `InstanceNormalization` in `utils/`.
- Reproduced training runs and saved histories (`hist*.pkl`) and the experiment notebook `training_results.ipynb`.
- Clear, reproducible setup using `requirements.txt` and a single Jupyter notebook to run experiments and visualize results.

## Tech stack & skills
- Languages / frameworks: Python, TensorFlow (Keras), Jupyter, Matplotlib, scikit-learn
- Concepts: Group Normalization, Instance Normalization, experimental comparisons, model evaluation, reproducibility

## Repository layout (important files)
- `training_results.ipynb`: Jupyter notebook containing the training code, comparison experiments, and plots.
- `utils/GroupNormalization.py`: Custom implementation of Group Normalization as a Keras layer.
- `utils/InstanceNormalization.py`: Custom implementation of Instance Normalization.
- `requirements.txt`: Minimal dependency list for reproducing experiments.
- `tiny-imagenet-200/`: Dataset folder (Tiny ImageNet-200). Contains `train/`, `val/`, `test/` and mapping files.
- `hist1.pkl`, `hist2.pkl`, `hist3.pkl`, `hist4.pkl`: Saved training histories (loss/accuracy curves) for quick visualization or further analysis.
- `E4040.2023Fall.NNDL.report.hm3008.yl5444.zl3372.pdf`: Final written report for the project.

## Quick setup (macOS / zsh)
1. Create and activate a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3. Run the experiments
- Start Jupyter and open `training_results.ipynb`:
```bash
jupyter lab
# or
jupyter notebook
```
- The notebook contains cells to load data, instantiate models (with GN/BN/IN/LN), train, and plot results.

## Notes about running
- This repo assumes the Tiny ImageNet-200 dataset is available under `tiny-imagenet-200/` in the project root. If it is not present, download and extract the Tiny ImageNet-200 dataset into that folder before running the notebook.
- Training can be GPU/time intensive — use a machine with a GPU for faster experiments.

## Results & artifacts
- Training curves and comparison plots are in `training_results.ipynb` and the `figures/` folder.
- Raw training histories are available in `hist1.pkl` .. `hist4.pkl` for re-plotting or statistical analysis.

## What I implemented / contributions
- Implemented `GroupNormalization` as a drop-in Keras layer (`utils/GroupNormalization.py`) following the original paper's approach and a stable implementation for TF2.
- Implemented `InstanceNormalization` (`utils/InstanceNormalization.py`) for baseline comparisons.
- Designed experiments comparing GN, BN, LN, and IN on a custom model architecture using Tiny ImageNet-200.

## How to evaluate / reproduce quickly
- Open `training_results.ipynb` and run the cells (or selectively run the training cells and then the plotting cells to reproduce figures).
- To reproduce a saved run, load one of the `hist*.pkl` files and plot the metrics (the notebook includes helper code for this).

## Next improvements (suggested)
- Add shell / Python training scripts for non-interactive runs (e.g., `train.py`) so CI and automated benchmarking are easier.
- Add a small README badge for license, Python version, and CI status after adding tests.
- Add example expected metrics (top-1 accuracy) and short summary table in the notebook for quick recruiter read-through.

## Contact / ownership
- Repo owner: `harindermashiana` (GitHub). If you'd like, I can add a short summary line with your email or LinkedIn for recruiter contact.

# Assignment   - Final Project Group Normalization

This project aims to reproduce the results of the paper “Group Normalization” by Yuxin Wu and Kaiming He. The goal is to evaluate the effectiveness of Group Normalization (GN) in comparison to Batch Normalization (BN), Layer Normalization (LN) and Instance Normalization (IN) on the Tiny ImageNet-200 dataset and model architecture we created. 

# How to use this repo

You can read the report attached in this repository for greater insights into the project. The entire code to run and reproduce the results in the original paper can be found in this notebook training_results.ipynb
