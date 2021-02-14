# Examples for Machine Learning Explainability Article
This repository is created for components for describing in this [article](https://medium.com/p/60aafa648b6f) about how Machine Learning model can be described for human understanding.

## Dataset
A dataset which is used in this project is originally published on [Kaggle](https://www.kaggle.com/mathan/fifa-2018-match-statistics)

## Prerequisite
- Git
- Python 3.8.7

## Setup
0. Clone the repository
```sh
git clone https://github.com/luangtatipsy/example-machine-learning-explainability.git
cd example-machine-learining-explainability
```
1. Create and activate a virtual environment for Python _(recommended)_. If you do not prefer using a virtual environment, skip to step 4.
```sh
python -m venv env
source env/bin/activate
```
2. Update pip to latest version
```sh
python -m pip install --upgrade pip
```

3. Install requirements
```sh
python -m pip install -r requirements.txt
```
4. Resolve issue of `pdpbox` package
- According to an [issue](https://github.com/SauceCat/PDPbox/issues/40). you have to locate a python file `pdp_plot_utils.py` (if you used virtual environment, it will be located at `env/lib/python3.8/site-packages/pdpbox/pdp_plot_utils.py`). Open the file and replace the line 251 from
```python
inter_ax.clabel(c2, contour_label_fontsize=fontsize, inline=1)
```
to
```python
inter_ax.clabel(c2, fontsize=fontsize, inline=1)
```

5. Serve a Jupyter Lab Server
```sh
python -m jupyter lab
```
then, you should be able to follow [`example.ipynb`](https://github.com/luangtatipsy/example-machine-learning-explainability/blob/main/example.ipynb)

## Acknowledgement
I would like to thank [Machine Learning Explainability Course](https://www.kaggle.com/learn/machine-learning-explainability) for creating the great course

## License
This repository is distributed under [MIT License](https://github.com/luangtatipsy/example-machine-learning-explainability/blob/master/LICENSE)
