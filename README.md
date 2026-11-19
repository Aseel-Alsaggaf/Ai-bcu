# Great Britain Road Casualties Dashboard (2021–2025)

## Run locally

Place `app.py`, `requirements.txt` and all three `.csv.gz` files in one folder.

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deploy to Streamlit Community Cloud

Upload these five files to a GitHub repository. In Streamlit Community Cloud select that repository and set the main file to `app.py`. Keep the `.csv.gz` files alongside `app.py`.

## Changes

- Clear geographic scope: **Great Britain**, not the whole United Kingdom.
- Collision severity is the single sidebar severity filter. Casualties and vehicles are linked to selected collisions by `collision_index`.
- Shows the limitations of independently cleaned datasets and the proportion of records that can be linked.
- Added a **Findings & actions** section based on the group's talking-points document, with careful wording about associations and causation.
- Clarified KSI casualty metrics vs serious/fatal collision metrics, including limitations of severity-filtered proportions.
- Preserved original visualisations and dataset download options.

## Important analytical limitations

The three input tables were cleaned independently, so some casualty and vehicle records cannot be linked to retained collisions. Dashboard linked totals will be lower than original cleaned-file totals, and neither should be described as complete official counts. Counts of recorded incidents cannot establish risk per trip or mile, and associations do not prove causation. Selecting only one collision severity makes severity percentages conditional and potentially uninformative. The accompanying original talking-points PDF refers to its own full-period analysis; re-check numeric claims against the current filtered dashboard before presenting.

## Verification

Python syntax checked and CSV schemas/joins inspected. A full interactive Streamlit browser test was **not** possible in this environment because Streamlit is not installed and package download access was unavailable. Please run locally or deploy and check all six/seven tabs before submission.
