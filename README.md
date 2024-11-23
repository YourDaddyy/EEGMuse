# SFU CMPT 340 Project - EEG Action Classification with Muse2 Brain Sensing Headband 
This project focuses on collecting, cleaning, and analyzing EEG data from the Muse2 Brain Sensing Headband. The goal is to classify user actions (e.g., scrolling or swiping) based on brain activity using machine learning models.


## Important Links

| [Timesheet](https://1sfu-my.sharepoint.com/:x:/g/personal/hamarneh_sfu_ca/EYcEhogX3nlMlobLCvc9I1UBQAROq3b5g4AKcHswM16LWg?e=0jHbXh) | [Slack channel](https://app.slack.com/client/T07K7SWL5A4/C07JKF7EBML) | [Project report](https://www.overleaf.com/project/66d0b103964b3acdf17669aa) |
|-----------|---------------|-------------------------|


- Timesheet: Link your timesheet (pinned in your project's Slack channel) where you track per student the time and tasks completed/participated for this project/
- Slack channel: Link your private Slack project channel.
- Project report: Link your Overleaf project report document.


## Video/demo/GIF
Record a short video (1:40 - 2 minutes maximum) or gif or a simple screen recording or even using PowerPoint with audio or with text, showcasing your work.


## Table of Contents
1. [Demo](#demo)

2. [Installation](#installation)

3. [Reproducing this project](#repro)

4. [Guidance](#guide)


<a name="demo"></a>
## 1. Example demo

A minimal example to showcase your work

```python
from amazing import amazingexample
imgs = amazingexample.demo()
for img in imgs:
    view(img)
```

### What to find where

Explain briefly what files are found where

```bash
repository
├── src                          ## source code of the package itself
├── scripts                      ## scripts, if needed
├── docs                         ## If needed, documentation   
├── README.md                    ## You are here
├── requirements.yml             ## If you use conda
```

<a name="installation"></a>
## 2. Installation

### Using `pip`:
1. Create a virtual environment:
    ```bash
    python -m venv .venv
    ```
2. Activate the virtual environment:
    - Windows: 
      ```bash
      .\.venv\Scripts\activate
      ```
    - Mac/Linux: 
      ```bash
      source .venv/bin/activate
      ```
3. Install dependencies:
    ```bash
    pip install matplotlib==3.9.2 pandas==2.2.3 scipy==1.14.1 mne==1.8.0 scikit-learn==1.5.2
    ```

### Using Conda:
1. Create and activate the Conda environment:
    ```bash
    conda create --name eeg_project python=3.10
    conda activate eeg_project
    ```
2. Install dependencies:
    ```bash
    conda install matplotlib==3.9.2 pandas==2.2.3 scipy==1.14.1 mne==1.8.0 scikit-learn==1.5.2
    ```

---

### Notes:
- Ensure you are using Python 3.10 or a compatible version.
- If additional packages are required, include them in the `requirements.yml` or `requirements.txt` file for consistency.

<a name="repro"></a>
## 3. Reproduction
Demonstrate how your work can be reproduced, e.g. the results in your report.
```bash
mkdir tmp && cd tmp
wget https://yourstorageisourbusiness.com/dataset.zip
unzip dataset.zip
conda activate amazing
python evaluate.py --epochs=10 --data=/in/put/dir
```
Data can be found at ...
Output will be saved in ...

<a name="guide"></a>
## 4. Guidance

- Use [git](https://git-scm.com/book/en/v2)
    - Do NOT use history re-editing (rebase)
    - Commit messages should be informative:
        - No: 'this should fix it', 'bump' commit messages
        - Yes: 'Resolve invalid API call in updating X'
    - Do NOT include IDE folders (.idea), or hidden files. Update your .gitignore where needed.
    - Do NOT use the repository to upload data
- Use [VSCode](https://code.visualstudio.com/) or a similarly powerful IDE
- Use [Copilot for free](https://dev.to/twizelissa/how-to-enable-github-copilot-for-free-as-student-4kal)
- Sign up for [GitHub Education](https://education.github.com/) 
