# Thai Music Genre Classification

This project was developed for the **Principles of Deep Learning** course.
It explores the classification of Thai music into four genres: Luk Thung,
Pop, Rock, and Hip-hop.

The project compares K-Nearest Neighbors (KNN) and a Neural Network using
audio features extracted from music preview clips.

## Repository Contents

- `01_Data_Cleaning/` — data cleaning notebook and original extracted feature data.
- `02_KNN/` — KNN notebook and cleaned feature data.
- `03_Neural_Network/` — Neural Network notebook and cleaned feature data.
- `04_Project_Report_and_Slides/` — project template and presentation slides.
- `05_Saved_Experiment/` — saved Model 3 and test data for reproducing the saved experiment results.
- `requirements.txt` — Python packages required to run the notebooks.

## Environment

The notebooks were run using **Python 3.14.6 on Windows (64-bit)**.

The package versions used are listed in `requirements.txt`.
The TensorFlow version used is `2.22.0rc0`, a release candidate.

## Setup

1. Download the repository using **Code → Download ZIP**, then extract it.
2. Install Python 3.14.6.
3. Open a terminal in the extracted repository folder and run:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open the project folder in VS Code and install the **Python** and
   **Jupyter** extensions if they are not already installed.
5. Open a notebook and select the Python environment where the packages
   were installed as its kernel.

## Running the Notebooks

Run each notebook with its own folder as the working directory so that
the CSV file can be found.

### 1. Data Cleaning

Open `01_Data_Cleaning/Data_Cleaning.ipynb`.

- `features.csv` contains the original audio features before cleaning.
- The notebook removes duplicate entries and short clips.
- After running, it saves the cleaned dataset as `features_clean.csv`
  in its working directory.

### 2. KNN

Open the notebook in `02_KNN/`.

This folder includes a copy of `features_clean.csv`, so the notebook can
be run without first running the data cleaning notebook.

### 3. Neural Network

Open the notebook in `03_Neural_Network/`.

This folder also includes a copy of `features_clean.csv`, so the notebook
can be run without first running the data cleaning notebook.

For each notebook, select **Restart Kernel**, then **Run All**.

## Notes

- The data is split by artist using `random_state=42`.
- The Neural Network is retrained when the notebook runs. Its results may
  vary between runs because of randomness during training.
- The Neural Network notebook saves Models 1, 2, and 3 in the `Saved/` folder.
  Running the notebook again may overwrite existing files with the same names.
