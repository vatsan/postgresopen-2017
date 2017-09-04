### [Scalable in-database machine learning with PL/Python](https://postgresql.us/events/schedule/pgopen2017/session/343-scalable-in-database-machine-learning-with-plpython/)

Date: 2017-09-08
Time: 11:30 - 12:20
Room: Market Street
Level: Intermediate

Enterprises who wish to build data driven machine learning applications should have access to technology that enables processing large volumes and flavors (structured, unstructured) of data efficiently and economically. There are vast collections of libraries for several specialized domains in the PyData ecosystem that are almost universally adopted by data scientists and engineers. Harnessing these libraries on a scalable platform/computation framework would help enterprises rapidly derive value from their data. In-database analytics brings computations to where the data resides, thereby reducing transport costs and I/O bottlenecks. PL/Python is a glue that binds the rich set of libraries in the PyData stack with the data residing in a Postgres database.

In this talk I'll demonstrate how to harness the power Python and it's ecosystem of data science and machine learning libraries to build statistical models for machine learning applications, in database on Postgres. I will begin with an overview of PL/Python on Postgres and describe concepts such as User Defined Functions (UDF) and Aggregates (UDA) in detail. I will then describe data parallel and model parallel machine learning problems with real world applications in Natural Language Processing (NLP) and illustrate with examples how to leverage libraries such as numpy, scipy, scikit-learn for solving them through PL/Python.

### Speaker

[Srivatsan Ramanujam](https://postgresql.us/events/schedule/pgopen2017/speaker/123-srivatsan-ramanujam/)

### Setting up your environment to run the demos

We encourage you to install Anaconda Python. If you haven't configured a `$HOME/.condarc` yet, we recommend you create one that looks like as shown below. If you already have a `$HOME/.condarc`, please update it suitable to reflect what is shown below.

```
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ cat ~/.condarc
envs_dirs:
  - $HOME/envs
pkgs_dirs:
  - $HOME/pkgs
``` 

Once you have Anaconda setup, you can replicate the virtual environment used for this project like so:

```
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ conda env create -f requirements-linux.yml 
```

This will create a virtual environment `postgresopen-2017` in your `$HOME/envs` folder. You can activate this environment by running:

```
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ source activate postgresopen-2017
(postgresopen-2017) vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ 
```

Copy and modify `env.sh.sample` to reflect the path to where you cloned this repo and source it.

```
(postgresopen-2017) vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ cp env.sh.sample env.sh
(postgresopen-2017) vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ cat env.sh
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ cat env.sh
export PROJECT_HOME=$HOME/code/postgresopen-2017
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ source env.sh
```

Start Jupyter by running the following:

```
(postgresopen-2017) vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ jupyter notebook
[I 02:23:26.433 NotebookApp] The port 8888 is already in use, trying another port.
[I 02:23:26.444 NotebookApp] Serving notebooks from local directory: /home/vatsan/code/postgresopen-2017
[I 02:23:26.444 NotebookApp] 0 active kernels 
[I 02:23:26.444 NotebookApp] The Jupyter Notebook is running at: http://localhost:8889/?token=1acb2f00465351610c26cfd3ac116cb95615a7bd28e7c931
[I 02:23:26.444 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```

Once completed, you may de-activate your virtual environment like so:

```
(postgresopen-2017) vatsan@vatsan-ubuntu:~/code/postgresopen-2017$ source deactivate
vatsan@vatsan-ubuntu:~/code/postgresopen-2017$
```

