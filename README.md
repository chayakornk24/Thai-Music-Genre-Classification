# Thai Music Genre Classification

This project was developed for the **Principles of Deep Learning** course.
It explores the classification of Thai music into four genres: Luk Thung,
Pop, Rock, and Hip-hop.

The project compares K-Nearest Neighbors (KNN) and a Neural Network using
audio features extracted from music preview clips.

## Repository Contents

- `Project Template.ipynb` — project overview, methodology, results, and discussion.
- `01_Data_Cleaning/` — data cleaning notebook and original feature data.
- `02_KNN/` — KNN notebook and cleaned feature data.
- `03_Neural_Network/` — Neural Network notebook and cleaned feature data.
- `Slides/` — presentation slides.

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

1. **Data Cleaning:** Open `01_Data_Cleaning/Data_Cleaning.ipynb`.
   It reads `features.csv` and creates `features_clean.csv`.
2. **KNN:** Open the notebook in `02_KNN/`. It reads the
   `features_clean.csv` provided in that folder.
3. **Neural Network:** Open the notebook in `03_Neural_Network/`.
   It reads the `features_clean.csv` provided in that folder.

For each notebook, select **Restart Kernel**, then **Run All**.

## Notes

- The data is split by artist using `random_state=42`.
- The Neural Network is retrained when the notebook runs. Its results may
  vary between runs because of randomness during training.
- The Neural Network notebook saves Model 3 to `Saved/model_3.h5`.
  Running it again may overwrite an existing file with the same name.
