# ITAI 1371 Lab 12: Ethics, Fairness, and Bias in ML

**Group:** JosephClay (individual submission)  
**Status:** Complete, ready to submit (November 16, 2026)

Train a logistic regression on the UCI Adult census data (predicting income over $50K), then audit it for fairness by sex: accuracy per group, and false positive / false negative rates per group.

## Results

| Metric | Men | Women | Gap |
|---|---|---|---|
| Accuracy | 81.20% | 91.81% | 10.61 points |
| False Positive Rate | 10.26% | 2.81% | 7.45 points |
| False Negative Rate | 37.80% | 47.84% | 10.04 points |

Overall accuracy: 84.61%. Decision: do not approve the model for hiring.

## Deliverables

```
ITAI1371_L12_Kit
├── submission/                                  What gets handed in
│   ├── L12_JosephClay_ITAI1371.pdf              Notebook, run top to bottom (0 errors)
│   ├── L12Journal_R_JosephClay_ITAI1371.pdf     Reflection journal (2 pages)
│   └── L12Journal_C_JosephClay_ITAI1371.pdf     Contribution journal (2 pages)
├── notebook/
│   └── L12_Ethics_Fairness_Bias_WORKING.ipynb   Source notebook with outputs
├── journals/
│   ├── Reflection_Journal_L12_JosephClay.md     Source for the reflection PDF
│   └── Contribution_Journal_L12_JosephClay.md   Source for the contribution PDF
├── README.md
└── .gitignore                                   kit/ and local tooling are not pushed
```

## How to run

```
python3 -m venv .venv
.venv/bin/pip install pandas scikit-learn ipykernel
```
Open `notebook/L12_Ethics_Fairness_Bias_WORKING.ipynb`, choose the `.venv` kernel, Run All. The first cell downloads `adult.data` from archive.ics.uci.edu, so it needs internet.

Known warnings (not errors): a `SyntaxWarning` for `sep=',\s*'` and a pandas notice that `dropna(inplace=True)` is deprecated.

## Notes

- The supplied notebook ("(2)" copy) already had code in the Task 1 and Task 2 cells and drafted conclusions in the Knowledge Check. The task code was run as given. This is disclosed in the contribution journal.
- Course slides and the reading were not available in this folder and were not reviewed.
- PDFs were exported with nbconvert (notebook) and headless Chrome.
