# Nawrot_CNS_Course
Teaching material CNS course

## Data Layout
The datasets used by the notebooks are now stored directly in this repository so that students can work in Google Colab after a single repository clone.

- `data/python_programming`
- `data/neural_data_analysis`
- `data/motor_cortex`

Each notebook contains a setup cell that clones the GitHub repository in Colab and defines the corresponding `DATA_DIR` path.

## Local Use Without Google Colab
Students who prefer to work locally can run the notebooks directly from a cloned copy of this repository.

```bash
git clone https://github.com/schmitfe/Nawrot_CNS_Course.git
cd Nawrot_CNS_Course
conda env create -f environment.yml -p ./.conda/nawrot-cns-course
conda activate ./.conda/nawrot-cns-course
jupyter lab
```

Open the notebooks from inside the cloned repository. The current setup cells detect whether they run in Colab or locally:

- in Colab they clone the repository into `/content/Nawrot_CNS_Course`
- locally they use the current repository folder as `REPO_ROOT`

If you work with an older notebook copy that still contains hard-coded Colab paths, replace paths of the form `/content/Nawrot_CNS_Course/...` with the corresponding local repository paths, for example:

- `/content/Nawrot_CNS_Course/data/motor_cortex/...` -> `REPO_ROOT / "data" / "motor_cortex" / ...`
- `/content/Nawrot_CNS_Course/data/neural_data_analysis/...` -> `REPO_ROOT / "data" / "neural_data_analysis" / ...`
- `/content/Nawrot_CNS_Course/data/python_programming/...` -> `REPO_ROOT / "data" / "python_programming" / ...`

In the current repository version, no further path edits should be necessary as long as the notebooks are started from the cloned repository.
