# Conda environment


## Install environment


- Step 1: Download this repository as zip-file (click on the green `<> Code`button at the top of this page and choose `Download ZIP`) button:

![](download.png)

---

- Step 2: Unzip the file in your *Downloads* directory.

---

- Step 3:
  - Mac: Open your [terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac#:~:text=Terminal%20for%20me-,Open%20Terminal,%2C%20then%20double%2Dclick%20Terminal.) and `cd` into the "environment" directory of your semester
  - Windows: Open your Anaconda Prompt and `cd` into the "environment" directory of your semester

Mac: (replace YourUserName with your actual username)

```bash
cd /Users/YourUserName/Downloads/environments-main/ws2425
```

Windows: open `Anaconda Prompt` (replace YourUserName with your actual username):

```bash
cd C:\Users\YourUserName\Downloads\environments-main\environments-main\ws2425
```

---

- Step 4: Replace the name "NAME_OF_ENVIRONMENT" with the environment of your choice 

```bash
conda env create -f NAME_OF_ENVIRONMENT.yml
```

For example, `env-lab`: 

```bash
conda env create -f env-lab.yml
```

That's it!

---

*If you want to use the environment, you simply need to type the name after "env", e.g. for "env-lab" lab:*

```bash
conda activate lab
```
