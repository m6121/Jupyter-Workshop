# Jupyter Workshop

This repository aims to introduce the idea of Jupyter notebooks in the context of open and reproducible research.
Originally these notebooks were developed as workshop for the integrated research training group at the CRC 1270 ELAINE (https://www.elaine.uni-rostock.de), later enhanced for the theme day 'Research Data Management' at the University of Greifswald and the graduate academy of the University of Rostock.

## License

[![Creative Commons License](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)

This work is if not otherwise stated licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
See the section below for third party contents and the corresponding licenses.

Please use the Zenodo reference:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4085067.svg)](https://doi.org/10.5281/zenodo.4085067)

In order to reference the GitHub repository, please attribute this as:

Max Schröder and Frank Krüger. “Jupyter Workshop,” https://github.com/SFB-ELAINE/Jupyter-Workshop

### Third Party Contents

This repository contains parts of other publications of open source software and data listed below:

1. The data in this repository in the `_data` folder has been converted from the ARFF files of the following publication of IMU data (CC-BY 4.0):
   Frank Krüger, Albert Hein, Kristina Yordanova and Thomas Kirste
   Recognising user actions during cooking task (Cooking task dataset) – IMU Data
   Rostock : Universität Rostock , 2017
   https://doi.org/10.18453/rosdok_id00000154
2. The two Jupyter notebooks `02 Python Introduction.ipynb` and `02 Python Introduction (Solutions).ipynb` are based on the repositories of:
   https://github.com/stefanluedtke/NLP-Exercises (MIT License) and https://github.com/spatialaudio/selected-topics-in-audio-signal-processing-exercises (CC0 1.0)

## Usage

This workshop material can be used for self-studies as well as for interactive workshops.
Notebooks are aimed to be worked through according to their numbering in the file name starting with `01 Introduction to Jupyter Notebooks.ipynb`.

*If you are using this material, make sure to check the License section.*

### Read-to-use Docker images

Despite the possibility to install Jupyter on your local computer e.g. by employing Anaconda, you also use Docker images.
In the following, we will describe the use of such an image:
`jupyter/scipy-notebook:latest`
For further information on the available images consult the corresponding documentation at https://jupyter-docker-stacks.readthedocs.io/en/latest/

```
$ docker run --rm \
    --name=jupyter-workshop \
    -p 127.0.0.1:8888:8888 \
    -v "$PWD":/home/jovyan/work \
    --user root \
    -e NB_UID=$(id -u) \
    -e NB_GID=$(id -g) \
    jupyter/scipy-notebook:latest
```

The parameters are used to configure the following aspects:

* `--rm`: remove the container after stopping,
* `--name=jupyter-workshop`: the container is named `jupyter-workshop`,
* `-p 127.0.0.1:8888:8888`: bind container port `8888` (3rd part) to the host ip address `127.0.0.1` at port `8888` (2nd part),
* `-v "$PWD":/home/jovyan/work`: connect the current directory `$PWD` to the container at `/home/jovyan/work`,
* `--user root`: needed to set the `UID` and `GID` of the user running inside the container in order to keep local permissions,
* `-e NB_UID=$(id -u)` and `-e NB_GID=$(id -g)`: to actually set the user and group ID to the same as on the host. This ensures write access to the volume mounted by `-v`.
