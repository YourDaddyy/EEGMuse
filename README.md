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
## 1. Example Demo

This section demonstrates how to run the web and upload the .

### Start the Web server

1. **Run Pipeline for cleaning data**:
   - Navigate to the `EEG_Web` directory:
     ```bash
     cd src/EEG_Web
     ```
   - Run the `server.py` script:
     ```bash
     python server.py
     ```
   - This script will:
     - Load the cleaned EEG dataset (`output.csv`).
     - Train a Random Forest model to classify user actions (e.g., scrolling or swiping).
     - Display accuracy metrics and results based on different random states.

2. **K-Nearest Neighbors (KNN) Classifier**:
   - From the same `models` directory, execute the `knn_classifier.py` script:
     ```bash
     python knn_classifier.py
     ```
   - This script will:
     - Train the KNN model using hyperparameter tuning.
     - Output the best accuracy along with an average performance summary across different runs.

### Visualizing EEG Data

1. **Scrolling EEG Data Visualization**:
   - Navigate to the `visualizations` directory:
     ```bash
     cd ../visualizations
     ```
   - Run the `visualize_scrolling_eeg.py` script:
     ```bash
     python visualize_scrolling_eeg.py
     ```
   - This script will generate EEG signal plots for scrolling actions, giving an insight into how EEG activity varies during these interactions.

2. **Swiping EEG Data Visualization**:
   - Execute the `visualize_swiping_eeg.py` script:
     ```bash
     python visualize_swiping_eeg.py
     ```
   - The script will produce visualizations of EEG signals during swiping actions, helping to understand the distinct patterns.

### End-to-End Example

This example walks through cleaning the data, extracting features, and training a classifier:

1. **Navigate to the `pipeline` directory**:
   ```bash
   cd ../pipeline
   ```
2. **Run the `pipeline.py` script**:
   ```bash
   python pipeline.py
   ```
   - This script will perform data cleaning, feature extraction, and model training in one go, offering an end-to-end demonstration of the entire workflow.

### Directory Overview

To make it easier to understand the project structure, here's a brief summary:

```bash
repository
├── src                          ## source code of the package itself
  ├── EEG_Data                   ## EEG data and process
  ├── EEG_Web                   ## If needed, documentation   
├── README.md                    ## You are here
├── requirements.yml             ## If you use conda
```

<a name="installation"></a>
## 2. Installation

To run this project, set up your development environment by following the steps below:

### Prerequisites:
- Ensure you have **Python 3.10** or a compatible version installed.
- Install a package manager (`pip` or `conda`).

### Using `pip`:
1. **Clone the Repository**:
    ```bash
    git clone git@github.com:sfu-cmpt340/2024_3_project_15.git
    ```
2. **Install Dependencies**:
    ```bash
    pip install -r requirements.yml
    ```

### Verifying the Setup:
1. Test the installation by running:
    ```bash
    python -c "import matplotlib, pandas, scipy, mne, sklearn; print('All dependencies are installed.')"
    ```

This ensures the environment is correctly set up and ready to run the project.

### Notes:
- Ensure you are using Python 3.10 or a compatible version.
- If additional packages are required, include them in the `requirements.yml` or `requirements.txt` file for consistency.

<a name="repro"></a>
## 3. Reproduction

Follow these steps to reproduce the results of this project:

### Step 1: Dataset Preparation
1. **Collect EEG Data**:
   - Use the Muse2 Brain Sensing Headband and the Muse Direct app to record raw EEG signals.
   - Save the recordings as CSV files for preprocessing.

2. **Preprocess the Data**:
   - Navigate to the data preprocessing directory:
     ```bash
     cd src/EEG_Data/dataCleaning
     ```
   - Run the cleaning script to remove noise and artifacts:
     ```bash
     python clean_data.py
     ```
   - This will generate a cleaned version of your dataset for feature extraction.

3. **Extract Features**:
   - Use feature extraction scripts to prepare the dataset for machine learning:
     ```bash
     python ./dataAnalyze/feature_extraction.py
     ```

4. **Result**:
   - The processed dataset (`output.csv`) will be saved in the `data` directory.

---

### Step 2: Model Training and Testing

1. Navigate to the `models` directory:
    ```bash
    cd src/EEG_Data/models
    ```

2. Train and test the models:

    - **Random Forest Classifier**:
      ```bash
      python random_forest.py
      ```

    - **K-Nearest Neighbors (KNN) Classifier**:
      ```bash
      python knn_classifier.py
      ```

3. Evaluate the performance:
    - Each script outputs:
        - Accuracy metrics.
        - Best random state for splitting the dataset.
        - Average accuracy across multiple random states.

4. Analyze the results:
    - Compare the performance of both models to determine which classifier works best for the given dataset.
    - Use the evaluation metrics to identify potential improvements, such as hyperparameter tuning or additional feature engineering.

## Troubleshooting

- **Muse Connection Issues**: Ensure Bluetooth is properly configured and your Muse headband is charged. Use `muse-lsl list` to confirm if the device is discoverable.
- **Dependency Errors**: Make sure all dependencies from `requirements.txt` are correctly installed. You may need to use a virtual environment to avoid conflicts.



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
