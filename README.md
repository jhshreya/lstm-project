# LSTM Next-Word Predictor

A small LSTM model, built with TensorFlow/Keras, that learns from a set of course FAQs and predicts the next word of a sentence. For example, starting from `"what is the fee"`, it keeps adding one predicted word at a time.

## Requirements

- **Python 3.12.** TensorFlow 2.21 does not support Python 3.13+ yet.
  - macOS: `brew install python@3.12`
  - Windows/Linux: download it from [python.org](https://www.python.org/downloads/)

## Setup

```bash
git clone https://github.com/jhshreya/lstm-project.git
cd lstm-project
python3.12 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Run

**Jupyter Notebook**

```bash
jupyter notebook main.ipynb
```

Then choose **Run → Run All Cells**.

**VS Code**

1. Open the `lstm-project` folder itself (not a parent folder) with **File → Open Folder…**
2. Open `main.ipynb`. Click **Select Kernel → Python Environments…** and pick `.venv (3.12.x)`, with the path `lstm-project/.venv/bin/python`.
3. Click **Run All**.

To check that the right kernel is active, run this in a cell:

```python
import sys; print(sys.executable)
```

It should print a path ending in `lstm-project/.venv/bin/python`.

## Troubleshooting

- **`ModuleNotFoundError: No module named 'tensorflow'`**: the notebook is using a different Python. Select the `.venv` kernel as described above, then restart the kernel.
- **`requires the ipykernel package`**: you selected the global Python instead of `.venv`. Don't install into it. Switch to the `.venv` kernel.
