# Conda environment

## Install environment


- Step 1: Download this repository as zip-file:

![](download.png)

---

- Step 2: Move the folder to a location (e.g. "MY_PATH") of your choice and unzip it.

---

- Step 3: Open your terminal and `cd` into the "environment" directory (replace MY_PATH with your path)

```bash
cd MY_PATH/environment
```

---

- Step 4: Replace the name "NAME_OF_ENVIRONMENT" with the environment of your choice (e.g. env-bigdata, env-ds, ...) 

```bash
conda env create -f NAME_OF_ENVIRONMENT.yml
```

---

- Step 5: Activate the environment (you simply need to type the name after "env", e.g. for "env-ds": ds):


```bash
conda activate ds
```

---

That's it! Now you can start to use this environment. For example, you could start a Jupyter Notebook with:

```bash
jupyter notebook
```

---

## Additional notes

Next time you start Anaconda, you will again need to avtivate your course-environment.


*If needed, you can deactivate the environment with (however, this is usually not necessary)* 

```bash
conda deactivate
```

## What is YAML?

YAML is a data serialization language that is often used for writing configuration files. The files contain text data arranged in a hierarchical structure and can be used as `.yaml` or `.yml`.

To learn more about `.yml` files, visit the following resources:

- [Creating an environment from an environment.yml file](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)

- [Creating an environment file manually](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually)
