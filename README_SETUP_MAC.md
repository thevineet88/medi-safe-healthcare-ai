MediSafe-Healthcare-AI
Local Setup & Launch Guide (macOS Only)

This guide explains how to set up, install dependencies, and run the MediSafe Flask web application and JupyterLab on macOS.

1. 🔧 Prerequisites (macOS)

Ensure the following are installed:

✔ Python 3.8+

Check version:

python3 --version

✔ Homebrew (optional but recommended)

Install if missing:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

✔ Git
git --version

2. 📁 Clone the Repository

Open Terminal and run:

git clone https://github.com/yogeshgirase29/MediSafe-Healthcare-AI.git
cd MediSafe-Healthcare-AI

3. 🧪 Create & Activate a Virtual Environment
Create .venv:
python3 -m venv .venv

Activate it:
source .venv/bin/activate


You should now see:

(.venv)


before your terminal prompt.

4. 📦 Install Dependencies

If requirements.txt exists:

pip install -r requirements.txt


If additional packages are needed:

pip install flask pandas numpy scikit-learn joblib

5. 🚀 Run the Flask Web Application

From the project root (same folder where app.py is located):

Option A — Recommended
python3 app.py

Option B — Using flask run (if needed)
export FLASK_APP=app.py
flask run

When the app starts, you will see:
Running on http://127.0.0.1:5000/


➡ Open this URL in your browser.

6. 🧪 Verify the Application

Once the interface opens, you should see the Medicine Safety Check form.

Test with sample inputs:

Example safe case:

Active Ingredient: Paracetamol

Expiry Date: 01/12/2026

Storage Temperature: 25

Warning Labels: 1

Dissolution Rate: 95

Disintegration Time: 10

Impurity Level: 0.3

Assay Purity: 99

This confirms the app is functioning properly.

7. 📓 Running JupyterLab (For Notebooks & ML Models)

You can explore datasets and training notebooks inside the src/ and Datasets_and_colabFiles/ folders.

Install JupyterLab (if not installed already):
pip install jupyterlab

Launch JupyterLab:
jupyter lab


This will open a browser window at:

http://localhost:8888/lab


Inside JupyterLab, you can open and run:

src/
Datasets_and_colabFiles/


These contain:

Model training notebooks

Dataset preprocessing steps

EDA & model selection experiments

8. 🛑 Stopping the App or JupyterLab

Press:

Ctrl + C


in the terminal running Flask or JupyterLab.

9. 🔁 Re-activating the Environment Later

Each time you reopen the project:

cd MediSafe-Healthcare-AI
source .venv/bin/activate
python3 app.py

10. 🧹 Deactivating the Virtual Environment
deactivate