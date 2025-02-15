# learned\_optimization: Meta-learning optimizers and more with JAX

[![Documentation Status](https://readthedocs.org/projects/learned-optimization/badge/?version=latest)](https://learned-optimization.readthedocs.io/en/latest/?badge=latest)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)


learned\_optimization is a research codebase for training learned
optimizers. It implements hand designed and learned optimizers, tasks to meta-train and meta-test them on, and outer-training algorithms such as ES, PES, and truncated backprop through time.

To get started see our [documentation](https://learned-optimization.readthedocs.io/en/latest/).

## Quick Start Colab Notebooks
Our our [documentation](https://learned-optimization.readthedocs.io/en/latest/) can also be run as colab notebooks! The fastest way to run is to leverage a free accelerator (TPU / GPU) in colab (go to `Runtime` -> `Change runtime type`). We have a 6 part introductory tutorial series here.

- 1. Introduction : <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part1_Introduction.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- 2. Creating custom tasks: <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part2_CustomTasks.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- 3. Creating custom tasks: <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part3_Truncation_TruncatedStep.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- 4. Gradient estimators: <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part4_GradientEstimators.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- 5. Meta training: <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part5_Meta_training_with_GradienLearner.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

- 6. Custom learned optimizers: <a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/Part6_custom_learned_optimizers.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>


Finally we have an entirely self contained, no dependency learned optimizer example.
<a href="https://colab.research.google.com/github/google/learned_optimization/blob/main/docs/notebooks/no_dependency_learned_optimizers.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>


## Local Installation
We strongly recommend using virtualenv to work with this package.

```
pip3 install virtualenv
git clone git@github.com:google/learned_optimizers.git
cd learned_optimizers
python3 -m venv env
source env/bin/activate
pip install -e .
```

## Train a learned optimizer example
To train a learned optimizer on a simple inner-problem, run the following:

`python3 -m learned_optimization.examples.simple_lopt_train --train_log_dir=/tmp/logs_folder`

A tensorboard can be pointed at this directory for visualization of results. (Note this will run very slowly without an accelerator.)

## Need help? Have a question?
File a github issue! We will do our best to respond promptly.

## Publications which use `learned\_optimization`
Wrote a paper or blog post that uses learned\_optimization? Add it to the list!

* Vicol, Paul, Luke Metz, and Jascha Sohl-Dickstein. ["Unbiased gradient estimation in unrolled computation graphs with persistent evolution strategies."](https://arxiv.org/abs/2112.13835) International Conference on Machine Learning (Best paper award). PMLR, 2021.
* Metz, Luke*, C. Daniel Freeman*, Samuel S. Schoenholz, and Tal Kachman. ["Gradients are Not All You Need."](https://arxiv.org/abs/2111.05803) arXiv preprint arXiv:2111.05803 (2021).

## Devlopment / Running tests
We locate test files next to the related source as opposed to a separate `tests/` folder.
Each test can be run directly, or with pytest -- (e.g. `python3 -m pytest learned_optimization/outer_trainers/`). Pytest can also be used to run all tests with `python3 -m pytest` (but this will take quite some time).

If something is broken please file an issue and we will take a look!

## Disclaimer

learned\_optimization is not an official Google product.
