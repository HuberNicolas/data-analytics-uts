<div align="center">

# Fundamentals of Data Analytics

**Coursework · 32130 Fundamentals of Data Analytics · University of Technology Sydney · Autumn 2024**

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![KNIME](https://img.shields.io/badge/KNIME-5.2-FDD800?logo=knime&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Poetry](https://img.shields.io/badge/Poetry-60A5FA?logo=poetry&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow)

[Contents](#contents) · [Getting started](#getting-started) · [Data](#data) · [Related repositories](#related-repositories)

</div>

My workshop work and assessment task 2 from the data analytics subject I took during an exchange semester at UTS:
KNIME workflows for classification and preprocessing, data exploration with pandas, and a scikit-learn pipeline that
classifies stars from Gaia data.

> [!NOTE]
> Unofficial study material, kept as submitted in 2024. Nothing is corrected, so answers can be wrong or incomplete.
> The notebooks were not re-run; the outputs are the original ones. The repository is not developed further. Demo
> notebooks, slides and assessment specifications from the teaching staff are not included, and neither are the
> assessment datasets (see [Data](#data)).

## Course

| | |
|---|---|
| Subject | 32130 Fundamentals of Data Analytics |
| Institution | University of Technology Sydney |
| Semester | Autumn 2024 (February to June), exchange semester from the University of Zurich |

## Contents

| Week / task | Topic | Files |
|---|---|---|
| Week 1 | KNIME: read Iris, filter columns, partition, train and score a decision tree, scatter plot | [workflow](workshops/week-01/w1-iris-workflow/), [notebook](notebooks/week-01.ipynb) (environment check) |
| Week 2 | KNIME preprocessing: remove duplicate rows and columns with missing values, write to Excel | [workflow](workshops/week-02/w2-iris-dataset/), [KNIME output](workshops/week-02/knime-output/) |
| Week 3 | Data exploration with pandas on Iris, Automobile, Abalone and Wine | [notebook](notebooks/week-03.ipynb), [data](workshops/week-03/) |
| AT2 | Classify the spectral type of stars from Gaia data: preprocessing pipeline, decision tree, k-NN, logistic regression, random forest, SVM and MLP, evaluated with ROC curves and confusion matrices | [notebook](assignments/at2-gaia-classification/at2-gaia-classification.ipynb) |

## Getting started

You need [Poetry](https://python-poetry.org/) and Python 3.12. The lock file is the one from March 2024.

1. Install the dependencies:

   ```bash
   poetry install --no-root
   ```

2. Start Jupyter:

   ```bash
   poetry run jupyter notebook
   ```

The KNIME workflows open in [KNIME Analytics Platform](https://www.knime.com/) 5.2 or later: **File → Import KNIME
Workflow** and choose the workflow folder.

## Data

| File | Source | License | Included |
|---|---|---|---|
| `workshops/week-0*/iris*.csv`, `iris*.xls` | [Iris](https://archive.ics.uci.edu/dataset/53/iris), UCI Machine Learning Repository (course copies, partly modified) | CC BY 4.0 | Yes |
| [`workshops/week-03/imports-85-1.csv`](workshops/week-03/imports-85-1.csv) | [Automobile](https://archive.ics.uci.edu/dataset/10/automobile), UCI | CC BY 4.0 | Yes |
| [`workshops/week-03/abalone-small-1-1.xls`](workshops/week-03/abalone-small-1-1.xls) | [Abalone](https://archive.ics.uci.edu/dataset/1/abalone), UCI (subset) | CC BY 4.0 | Yes |
| [`workshops/week-03/wine-2.xls`](workshops/week-03/wine-2.xls) | [Wine](https://archive.ics.uci.edu/dataset/109/wine), UCI | CC BY 4.0 | Yes |
| `assignments/at2-gaia-classification/data/dataGaia_AB_train.csv` | Prepared by the teaching staff from [Gaia DR3](https://www.cosmos.esa.int/web/gaia/dr3) (ESA) | Unclear for the prepared file | No |

To re-run AT2, put the course file into `assignments/at2-gaia-classification/data/`.

## Known issues

- The AT2 notebook imports TensorFlow and tqdm, which were never added to `pyproject.toml`. Poetry cannot pin their
  dependencies to the 2024 versions, so they are left out. Install them separately if you need them.
- `lineapy` is in `pyproject.toml` but unused, and it fails to import with pydantic 2. It does not affect the notebooks.
- The KNIME reader and writer nodes point to absolute paths on my old machine. Reconfigure them to the files in the
  workflow's week folder.

## Related repositories

Other subjects from the same exchange semester at UTS:

| Subject | Repository |
|---|---|
| 32130 Fundamentals of Data Analytics | this repository |
| 42037 IoT Security | [iot-security-uts](https://github.com/HuberNicolas/iot-security-uts) |
| Python Programming for Data Processing | [python-data-processing-uts](https://github.com/HuberNicolas/python-data-processing-uts) |
| 32547 UNIX Systems Programming | [unix-systems-programming-uts](https://github.com/HuberNicolas/unix-systems-programming-uts) |

## Acknowledgements

- Fisher, R. A. (1936). *Iris* [Dataset]. UCI Machine Learning Repository. <https://doi.org/10.24432/C56C76>
- Schlimmer, J. (1987). *Automobile* [Dataset]. UCI Machine Learning Repository. <https://doi.org/10.24432/C5B01C>
- Nash, W., Sellers, T., Talbot, S., Cawthorn, A., & Ford, W. (1995). *Abalone* [Dataset]. UCI Machine Learning
  Repository. <https://doi.org/10.24432/C55C7W>
- Aeberhard, S., & Forina, M. (1991). *Wine* [Dataset]. UCI Machine Learning Repository. <https://doi.org/10.24432/C5PC7J>
- This work has made use of data from the European Space Agency (ESA) mission
  [Gaia](https://www.cosmos.esa.int/gaia), processed by the Gaia Data Processing and Analysis Consortium
  ([DPAC](https://www.cosmos.esa.int/web/gaia/dpac/consortium)).

## License

My own code, notebooks and KNIME workflows are licensed under the [MIT License](LICENSE). The datasets keep their own
licenses (see [Data](#data)).

## Author

Nicolas Huber ([@HuberNicolas](https://github.com/HuberNicolas)), exchange student at UTS in Autumn 2024.
