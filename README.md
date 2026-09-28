# Duke University IDS-789: Fundamentals of Finance Business Models

Resources for the IDS 789 final project: last year's final projects, plus sample notebooks you can use as starter code or for project ideas.

## Repository Structure

```
Duke-IDS789/
├── Fall 2025/          # Final projects from last year (papers + presentations)
├── Sample Projects/    # Reference notebooks with data, one folder per project
└── requirements.txt
```

## Fall 2025: Past Final Projects

The final research papers and presentations from the five Fall 2025 teams. Use them to see what a finished project looks like: its scope, structure, and level of depth.

| Team | Research Paper | Presentation |
|------|----------------|--------------|
| Team 1 | [PDF](<Fall 2025/Team1 Final Research Paper -Fall 2025.pdf>) | [PDF](<Fall 2025/Team1 Final Presentation- Fall 2025.pdf>) |
| Team 2 | [PDF](<Fall 2025/Team2 Final Research Paper -Fall 2025.pdf>) | [PPTX](<Fall 2025/Team2 Final Presentation- Fall 2025.pptx>) |
| Team 3 | [PDF](<Fall 2025/Team3 Final Research Paper -Fall 2025.pdf>) | [PDF](<Fall 2025/Team3 Final Presentation -Fall 2025.pdf>) |
| Team 4 | [PDF](<Fall 2025/Team4 Final Research Paper - Fall 2025.pdf>) | [PPTX](<Fall 2025/Team4 Final Presentation- Fall 2025.pptx>) |
| Team 5 | [PDF](<Fall 2025/Team5 Final Research Paper - Fall 2025.pdf>) | [PPTX](<Fall 2025/Team5 Final Presentation  -Fall 2025.pptx>) |

## Sample Projects

Each folder has a Jupyter notebook and the data it uses. The notebooks are meant as references and starting points: reuse the methods, swap in different data, or extend the analysis for your own project.

| Project | Topic | Methods | Data |
|---------|-------|---------|------|
| [Deposit Subscription Prediction](<Sample Projects/Deposit Subscription Prediction>) | Predict which customers will subscribe to a term deposit (CD) | Decision tree, MLP classifier, feature importance | [Kaggle: Predict Term Deposit](https://www.kaggle.com/datasets/aslanahmedov/predict-term-deposit) |
| [Interest Rate Prediction](<Sample Projects/Interest Rate Prediction>) | Forecast Treasury yields from past values | MLP regressor on lookback windows | [U.S. Treasury Daily Yields](https://home.treasury.gov/resource-center/data-chart-center/interest-rates) |
| [Loan Approval Prediction](<Sample Projects/Loan Approval Prediction>) | Predict whether a loan application will be approved | Decision tree, feature importance | [Kaggle: Eligibility Prediction for Loan](https://www.kaggle.com/datasets/devzohaib/eligibility-prediction-for-loan) |
| [Loan Delinquency Prediction](<Sample Projects/Loan Delinquency Prediction>) | Predict delinquency on Fannie Mae single-family mortgages | Decision tree; parsing the column layout from the provided PDF | [Fannie Mae Loan Performance Data](https://capitalmarkets.fanniemae.com/credit-risk-transfer/single-family-credit-risk-transfer/fannie-mae-single-family-loan-performance-data) (sample) |
| [Mortality Risk](<Sample Projects/Mortality Risk>) | Price life insurance premiums from survival curves for smokers vs. non-smokers | Hazard rates, survival functions, discounted premiums | Mortality table (`.xlsx`, included) |
| [Pricing Callable CD](<Sample Projects/Pricing Callable CD>) | Find the fair rate on a CD the bank can call early | Interest-rate modeling, Monte Carlo simulation, autocorrelation | U.S. Treasury daily rates (included) |

## Setup

The notebooks use Python 3 with numpy, pandas, matplotlib, seaborn, scikit-learn, statsmodels, PyPDF2, and openpyxl.

Create a conda environment and register it as a Jupyter kernel:

```bash
conda create -n ids789 -c conda-forge python=3.12 numpy pandas matplotlib seaborn scikit-learn statsmodels pypdf2 openpyxl ipykernel
conda activate ids789
python -m ipykernel install --user --name ids789 --display-name "Python (ids789)"
```

Then open a notebook and select the **Python (ids789)** kernel. In VS Code, click **Select Kernel** in the top-right corner of the notebook, then choose **Jupyter Kernel... → Python (ids789)**.

> **Note:** `requirements.txt` pins older versions and includes Linux-only packages (CUDA, triton, torch), so it will not install on macOS or Windows. Use the conda command above instead.

Notebooks load their data by file name, so run each one from inside its own folder. Jupyter and VS Code do this by default.
