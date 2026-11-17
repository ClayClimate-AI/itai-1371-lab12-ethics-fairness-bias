# Contribution Journal: Lab 12, Ethics, Fairness, and Bias in ML

**Name:** Joseph Clay  
**Group name:** JosephClay  
**Group members:** Joseph Clay (individual submission)  
**Course:** ITAI 1371  
**Date:** November 16, 2026  

## 1. My contributions

I worked on this lab in sessions on November 12 and November 16, 2026.

| What I did | Where it is |
|---|---|
| Reviewed the lab kit (README and BRIEF) and planned the work in stages | Lab folder |
| Found that the supplied "(2)" notebook already had code in the Task 1 and Task 2 cells and drafted conclusions in the Knowledge Check | Lab folder |
| Set up a Python virtual environment with pandas, scikit-learn, and Jupyter, and set it as the notebook kernel in VS Code | `.venv/`, `.vscode/settings.json` |
| Ran the notebook and recorded the results: overall accuracy 84.61%, accuracy 81.20% (men) and 91.81% (women), FPR 10.26% / 2.81%, FNR 37.80% / 47.84% | Working notebook |
| Filled in all result values in the Knowledge Check and worked out the size of the accuracy gap (10.61 points) | Working notebook, Knowledge Check cell |
| Chose the answers in the Knowledge Check and wrote my own justification for not approving the model for hiring | Working notebook, Knowledge Check cell |
| Corrected my FPR answer from Females to Males after checking it against my output, and answered that there is a significant difference between the groups | Working notebook, Knowledge Check cell |
| Wrote my reflection on accuracy, subgroup performance, error types, and my deployment decision | `L12Journal_R_JosephClay_ITAI1371.pdf` |
| Re-ran the full notebook top to bottom with no errors and exported it to PDF | `L12_JosephClay_ITAI1371.pdf` |
| Cleaned up the project folder, removing the unused journal templates | Lab folder |

## 2. Code I ran and checked

- **Setup cell (given):** loads the UCI Adult census data, drops rows with missing values (32,561 rows down to 30,162), maps income to 0/1, makes a 70/30 stratified split, and trains a logistic regression in a pipeline with `StandardScaler` and `OneHotEncoder`.
- **Task 1 and Task 2 cells:** these were already filled in when I received the "(2)" notebook. I ran them as given and did not change the code. Task 1 computes accuracy for men and women separately. Task 2 computes FPR = FP / (FP + TN) and FNR = FN / (FN + TP) for each group from the confusion matrix.
- **Result:** the notebook ran top to bottom with no errors. There are two warnings that do not affect the results: a `SyntaxWarning` for the `'\s'` separator and a pandas notice about `dropna(inplace=True)`.

## 3. Documentation I wrote

- **Knowledge Check:** result values for both tasks; the accuracy gap of 10.61 points; that the model performs better for women by accuracy; that men have the higher FPR; my decision not to approve the model for hiring with my justification; and why removing the `sex` column would not remove proxy bias.
- **Reflective journal:** how overall accuracy can hide unequal outcomes, why a higher accuracy for one group does not mean the model is fair to it (women had the highest accuracy but also the highest FNR, 47.84%), the difference between false positives and false negatives, and my deployment decision.

## 4. Team members' contributions

I completed this lab on my own. There were no other group members.

## 5. Tools I used

I used Claude Code (an AI assistant) for mechanical tasks: reviewing the kit, setting up the virtual environment and the VS Code kernel setting, explaining the kernel picker, reading results out of the notebook, pointing out that my FPR answer named the wrong group and that I had not picked "is / is not" for significance, then making those two edits after I chose the answers, formatting my reflection and adding my result numbers to it, renaming the working notebook, re-running and exporting the notebook and journals to PDF, and drafting this contribution journal from a record of the sessions. The Task 1 and Task 2 code came with the supplied notebook. The Knowledge Check answers and my reflection are my own.

## 6. What I would do differently

I would ask the instructor at the start about the "(2)" notebook that already had code and conclusions in it, and get a blank starter if needed. I would also check every answer against my printed output before moving on, since I named the wrong group for the higher FPR the first time.
