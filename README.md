# E-Commerce Customer Churn Prediction & Risk Analytics using RFM and Machine Learning

**Rohit Dey** · AICTE | IBM SkillsBuild Data Analytics with AI Academic Internship 2026 · BharatCares


## Verified student and internship details

- **Name:** Rohit Dey
- **Institution:** Guru Gobind Singh Educational Society's Technical Campus
- **Program:** IBM SkillsBuild Data Analytics with AI Internship 2026
- **Conducted by:** BharatCares, in association with AICTE and IBM SkillsBuild
- **Mode:** Virtual
- **Scheduled period:** 17 August 2026–30 September 2026
- **Stated duration:** 6 weeks, as described in the offer letter
- **GitHub:** https://github.com/Rohitdey45
- **Repository:** https://github.com/Rohitdey45/RohitDey-ECommerce-Customer-Churn-Analytics

Institution and schedule are verified from the student-supplied offer letter issued on 22 August 2026. Course, branch, semester and mentor details were not provided and are not invented. Scheduled dates do not imply successful completion. Internship ID and signature are intentionally omitted from the public README; do not publish the signed offer letter.

### Additional offer-letter guidance
The letter mentions SDG-aligned project development and Week 6 “PPT and Project” submission/presentation. The supplied Google Form shows four document/code upload fields, not a PPT field. Confirm whether a presentation/PPT is required separately. Potential conceptual relevance to **SDG 9 — Industry, Innovation and Infrastructure** is limited to digital analytical capability; no SDG target achievement or measured sustainability impact is established. The actual supplied masterclass decks/workbook, rather than the differently numbered administrative timetable, govern the project's technical workflow.

## Public source-only repository
This privacy-conscious copy contains the notebook **without outputs**, tested requirements, document-generation code, aggregate evaluation/audit results and data acquisition instructions. Executed submission report, interactive dashboard, transaction records and customer-level exports are intentionally omitted. They can be generated locally using authorized source data. The four Google Form files are supplied separately in the student submission package.

## Dataset
Dataset: Official Masterclass 1 Practice Dataset provided with the IBM SkillsBuild Data Analytics with AI internship materials.

[INSERT OFFICIAL DATASET LINK IF PROVIDED BY TRAINER]

No verified public dataset URL is available. Obtain the official 95-page PDF export from the trainer. Put it in `data/` under `AI + Data_ Make Data Intelligent _ Masterclass 1 _ Practice Dataset.pdf`. The notebook checks the inspected page layout and reconstructs a local workbook; it does not claim original Excel sheets or types. No Kaggle or supermarket data are used. Data redistribution permission is not assumed.

## Problem and methodology
Describe sales and create historical customer RFM features, then predict no recorded purchase over a later 180-day window. Audited cleaning → EDA → customer aggregation → RFM → leakage-safe target → Logistic Regression → held-out evaluation → probabilities → risk bands → dashboard → cautious business action.

Features use 1 January–21 February 2026; outcomes use 22 February–20 August 2026. The 204-customer cohort contains 27 future-inactive customers. This follows the workbook's predictive 180-day guidance while explicitly documenting its inconsistent 90-day and combined frequency/monetary definitions.

## Actual evaluation and limitations
Held-out accuracy 86.27%, precision 0, recall 0, F1 0, ROC-AUC 0.6526. Accuracy matches the majority baseline. All seven inactive test customers are missed at threshold 0.50. Do not deploy as an automated churn detector. Classroom risk bands remain <40% Low, 40%–<70% Medium, ≥70% High; no historical customer reaches High Risk.

Short history, PDF reconstruction, missing values, small positive test class, unverified observation completeness and a single-snapshot random customer split limit validity. No causal mechanism or retention ROI is established. Longer history, temporal backtesting, calibration and a randomized retention pilot are future work.

## Setup and execution
Python 3.11+; tested on Python 3.13.

```bash
python -m venv .venv
# Activate .venv for your operating system, then:
python -m pip install -r requirements.txt
jupyter notebook
```

Run all notebook cells from this repository root after placing the authorized PDF in data/. It creates local outputs, charts and an offline Plotly dashboard. Run `python scripts/create_documents.py` afterward to create the Word report and full local README. The generated full README describes local/private files and is **not** a replacement for this public README without a privacy review. Do not publish generated customer/data outputs unless permitted.

## Contents
```text
RohitDey_ECommerceCustomerChurnPrediction.ipynb  # outputs cleared
requirements.txt
README.md
.gitignore
data/README.md
scripts/create_documents.py
scripts/prepare_public_repository.py
outputs/                                    # aggregate metrics/audits only
```

## Data dictionary
Actual columns: Order_ID (order key), Order_Date (purchase date), Customer_ID (coded customer key), Product, Category, Region (city label), Quantity (units), Revenue (INR), Profit (INR). The notebook preserves actual source column names. Customer identifiers are never prediction features.

## Business interpretation
Use the dashboard and audit to investigate patterns, not claim model success. Precision/recall have different contact-budget and missed-customer implications. Validate before using scores for retention; observations and hypotheses are separated in the notebook. Raw/source data remain local.

## References and author
Supplied Masterclass 1 and 2 decks and Masterclass 3 student workbook are the primary learning references. Supermarket report is a structural example only. Source PDF and submission-form screenshots were supplied by the student. AI assisted code/documentation preparation; numerical results were executed against the official practice PDF. Author: Rohit Dey.
