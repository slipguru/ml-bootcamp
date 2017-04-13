# ml-bootcamp
A series of tutorials complete with notebook to learn the basic principle of machine learning techniques

## Abstract

In the learning from example paradigm, given a limited amount of data in the form of input-output pairs (x, y) we want to learn the relationship between inputs and output by using a learning algorithm to infer a function such that, for any given input, it is able to determine the corresponding output.

Moreover, for high dimensional data (i.e., when the dimensionality of the input is high, as in the order of the thousands or more), it is reasonable to assume that only a small subset of the available variables is relevant, i.e. is sufficient to infer the aforementioned function.

However, when dealing with real-life datasets such as molecular high-throughput data, it is common to have a number of samples which is significantly smaller than the number of dimensions. This may lead to issues in determining the outcome of the analysis, especially if the signal to noise ratio in the data is low.

In this tutorial I will start from the very basics of supervised learning, reviewing state of the art algorithms for supervised learning and variable selection.
I will perform experiments on synthetic and real datasets using several machine learning packages such as scikit-learn. All examples will be provided in the form of Jupyter notebooks.
Finally, I will present a variable selection framework we developed, which is designed to work on clusters using MPI for the parallelization.

## Installation instructions

**NOTEBOOKS HERE**: https://www.dropbox.com/s/wzxo32zv86tt5ou/notebookx.zip?dl=0

I strongly suggest using **miniconda** so that you can create a virtual environment and pack everything in a single folder which you can nuke at will as soon as the tutorial is over in case you're not satisfied :)

The installation should take a few minutes. I suggest you to do it _before_ the tutorial as 30 people downloading stuff with the connection provided by the hotel we will be at might cause some problems.

### Linux and OSX

Here are all the steps you need to install miniconda and create a virtual environment with all required packages for this tutorial. I assume you're using either Linux or OSX (anything unix-based will do). I honestly never installed it on Windows, however I assume that it should not be that hard (and I believe in you!) and at some point (probably around the time you start creating the virtual environment) the instructions should be the same for all OS.

**Step 1**: Download `miniconda` from https://conda.io/miniconda.html
```
$ wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

**Step 2**: Install `miniconda` on your laptop. When asked if you want to add the installation path of miniconda to the `$PATH` environment variable say `yes`, as the ghostbusters taught us. You might have to open a new shell so that the `$PATH` environment variable refreshes properly.

```
$ bash Miniconda3-latest-Linux-x86_64.sh
```

**Step 3**: Create a virtual environment. Because of reasons, please specify `python=2` so that it will create an environment with `Python 2` installed. Once it has been created, you have to _activate_ it.

`$ conda create --name palladio python=2`  
`...`  
`$ source activate palladio`

**Step 4**: Install the package `palladio` using pip. `palladio` is a framework which we will use in the tutorial, and it requires several other packages that will be automatically downloaded. Then, install (using either `conda` or `pip`, they both should work) two additional packages, `jupyter` and `ipython` (probably `ipython` is a requirement for `jupyter` so it's automatically installed).

`(palladio) $ pip install palladio`  
`(palladio) $ conda install jupyter ipython`

### Windows

I assume that you installed anaconda Navigator.

Create an environment specifying Python version 2.*.
Install packages `scikit-learn` (which should automatically install numpy and scipy), `joblib`, `seaborn` and `jupyter` using the tool from the navigator.

Open a terminal (play button -> open terminal) and install `palladio` using `pip install palladio`.

Done! You should be good to go. In order to check if everything's good, open a jupyter notebook (from the shell just enter `jupyter-notebook`, a new browser window should appear) and try to import `palladio`. If you don't get any error messages, it's done! You might get a warning about a missing mpi4py library, don't worry about it.

If you get stuck for any reason during the installation process feel free to contact me! I'm actively developing the framework and we're still working on the deployment phase so we're more than happy to receive feedback.

See you soon!