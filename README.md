# Discriminatory Text Detection on Fedora Mailing List

## Overview

_Current Open Source Software (OSS) communities have many avenues of communication available to them, including mailing lists, chat channels, and forum boards. 

Mailing lists have become popular targets for mining sentiment and emotions, as they usually provide a centralized communication hub for members of a distributed OSS community. Sentiment and emotions within communities can provide insights into community health. Good community health will help with initiatives aimed at fostering positive interactions between OSS community members, strengthening social ties, and helping the community accomplish its tasks.

With that, the task of conducting sentiment analysis on the Fedora user and developer mailing list found its roots. Over the summer, the project evolved into being focused on hate speech and offensive language detection. Through the next few months, there will be multiple combinations of models and training sets tested to see which gives the best accuracy. A service then will be developed that can be used to analyze any OS mailing list data.

The goal of this service is to be able to provide community managers information about how their community communicates with one another. In an ideal world, the service would notify manager of threads or users that are turning towards discriminatory language that could push away other members from wanting to contribute. _

## A. Problem Statement:

_Through the the data from the devel and user Fedora Mailing List, create a model that best detects if a given email or thread is conducting "offensive" or "discriminatory" language. From this model, develop a service that community managers can use to be notified of this behavor/ analyze over time the changes in this sector of sentiment._ 

1. Clean the data set 
2. Create a train, testing, and validation data set
3. Create a model that best labels the emails into the 3 categories 
4. Look into using this analysis to determine the health of threads 
5. Deploy into a service for community managers 

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── Pipfile            <- Pipfile stating package configuration as used by Pipenv.
    ├── Pipfile.lock       <- Pipfile.lock stating a pinned down software stack with as used by Pipenv.
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file stating direct dependencies if a library
    │                         is developed.
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    ├── .thoth.yaml        <- Thoth's configuration file
    ├── .aicoe-ci.yaml     <- AICoE CI configuration file (https://github.com/AICoE/aicoe-ci)
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
