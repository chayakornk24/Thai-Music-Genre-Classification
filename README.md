# Thai Music Genre Classification

This project was developed for the **Principles of Deep Learning** course.
It explores the classification of Thai music into four genres: Luk Thung,
Pop, Rock, and Hip-hop.

The project compares **K-Nearest Neighbors (KNN)** and a **Neural Network**
using audio features extracted from music preview clips.

## Repository Contents

| Folder / File | Description |
|---|---|
| `01_Data_Cleaning/` | Data cleaning notebook and original extracted feature data. |
| `02_KNN/` | KNN notebook and cleaned feature data. |
| `03_Neural_Network/` | Neural Network notebook and cleaned feature data. |
| `04_Project_Report_and_Slides/` | Project template and presentation slides. |
| `05_Saved_Experiment/` | Saved Model 3 and test data for evaluating the saved experiment. |
| `requirements.txt` | Python packages required to run the notebooks. |

## Environment and Setup

The notebooks were run using **Python 3.14.6 on Windows (64-bit)**.

The package versions are listed in `requirements.txt`. The TensorFlow
version used is `2.22.0rc0`, a release candidate.

### Installation

1. Download the repository using **Code → Download ZIP**, then extract it.
2. Install Python 3.14.6.
3. Open a terminal in the extracted repository folder and run:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open the project folder in VS Code. Install the **Python** and
   **Jupyter** extensions if they are not already installed.
5. Open a notebook and select the Python environment where the packages
   were installed as its kernel.

## Running the Notebooks

Run each notebook with its **own folder as the working directory** so that
it can find the required files.

For each notebook, select **Restart Kernel**, then **Run All**.

### 1. Data Cleaning

Open `01_Data_Cleaning/Data_Cleaning.ipynb`.

- `features.csv` contains the extracted audio features before cleaning.
- The notebook removes duplicate entries and short clips.
- It saves the cleaned data as `features_clean.csv` in its working directory.

### 2. KNN

Open the notebook in `02_KNN/`.

The folder includes a copy of `features_clean.csv`, so the notebook can
be run without first running the data cleaning notebook.

### 3. Neural Network

Open the notebook in `03_Neural_Network/`.

The folder also includes a copy of `features_clean.csv`, so the notebook
can be run without first running the data cleaning notebook.

### 4. Saved Experiment

Open `05_Saved_Experiment/View_Saved_Results.ipynb`.

This notebook loads the saved Model 3 and test data to evaluate the saved
experiment **without retraining**. It reports Top-1 and Top-2 accuracy.

## Notes on Reproducibility

- The data is split by artist using `random_state=42`.
- The main Neural Network notebook retrains the models when run. Results
  may vary between runs because of randomness during training.
- The Neural Network notebook saves Models 1, 2, and 3 in the `Saved/`
  folder. Running it again may overwrite existing files with the same names.
- The saved experiment can be evaluated without retraining.

## Additional Analysis: Top-2 Accuracy

Top-2 accuracy was not covered in the course. During error analysis, we
observed that some songs may have characteristics of more than one genre,
while each clip has only one label in the dataset.

We used AI assistance to help write the code for calculating Top-2 accuracy.
This metric checks whether the true label is among the model's two
highest-scoring predictions.

## Educational Use and Data Source

This project was developed for educational purposes as part of the
Principles of Deep Learning course. It is not intended for commercial use.

Music metadata and preview information were obtained through the
iTunes Search API. Song titles, artist names, artwork, and other
third-party content remain the property of their respective rights holders.

This repository contains extracted audio features and project code.
It does not distribute the original music recordings or preview audio.
