# Cookiecutter Data Science

This is a bridge between the https://github.com/hackalog/bus_number/blob/master/TUTORIAL.md and  drivendata/cookiecutter-data-science

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._

Parent Project:
#### [Project homepage](http://drivendata.github.io/cookiecutter-data-science/)

I have customized the cookiecutter template to meet my requirements

### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter -c v1 https://github.com/mh4ey/cookiecutter-data-science


[![asciicast](https://asciinema.org/a/244658.svg)](https://asciinema.org/a/244658)

### New version of Cookiecutter Data Science
------------
Cookiecutter data science is moving to v2 soon, which will entail using
the command `ccds ...` rather than `cookiecutter ...`. The cookiecutter command
will continue to work, and this version of the template will still be available.
To use the legacy template, you will need to explicitly use `-c v1` to select it.
Please update any scripts/automation you have to append the `-c v1` option (as above),
which is available now.


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```
├── LICENSE
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
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
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
├── src                <- Source code for use in this project.
│   ├── __init__.py    <- Makes src a Python module
│   │
│   ├── data           <- Scripts to download or generate data
│   │   └── make_dataset.py
│   │   └── fetch_dataset.py
│   │
│   ├── features       <- Scripts to turn raw data into features for modeling
│   │   └── build_features.py
│   │
│   ├── models         <- Scripts to train models and then use trained models to make
│   │   │                 predictions
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   └── visualization  <- Scripts to create exploratory and results oriented visualizations
│       └── visualize.py
│
└── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io
```
## make environment
You can edit the environment.yml file to include/exclude packages needed by your project.

After having edited the list of packages needed by your project, you can execute the command
    
    make environment
to create environment

If you have done this step before, and you want to update the environment, you need to run

   make update_environment

## Contributing

Adding your Project repository to Github
If you follow the instructions from above, you should have

Downloaded the repository
Created your own project with the desired file and folder structure
Created your working environment for you project
The next step is to add it to Github and make it accessible.

To do this, your should do the following:

Create a Github repository with the same name as the repository.
Type git add remote origin git@github.com:<username>/<project_name>.git. In here you need to replace <username> and project_name with your details.
git push origin master - This will push your project to Github.
To check that you did this correctly, type

git remote -v
and you should get something that looks like this:

origin  https://github.com/<username>/<project_name>.git (fetch)
origin  https://github.com/<username>/<project_name>.git (push)
where username and project_name pertain to your repository on Github.

Now all of the files are online on Github, and should be ready to integrate them with Read The Docs.
 
credit: https://cookiecutter-data-science-vc.readthedocs.io/en/latest/getting_started/INSTALL.html

### Installing development requirements
------------

    pip install -r requirements.txt

### Running the tests
------------

    py.test tests
