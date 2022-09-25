# Conda environment

- Download this repository as zip-file:

![](download.png)

- Open your terminal and `cd` into the "environment" directory (replace YOUR_PATH_TO with your path)

```bash
cd YOUR_PATH_TO/environment
```

- Replace the name "NAME_OF_ENVIRONMENT" with the environment of your choice (e.g. env-bigdata, env-ds) 

```bash
conda env create -f NAME_OF_ENVIRONMENT.yml
```

- Activate the environment (e.g. for env-ds):

```bash
conda activate ds
```
