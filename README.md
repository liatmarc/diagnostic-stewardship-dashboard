# Pediatric Diagnostic Stewardship – Static Dashboard (Simulated Data)

This folder contains a **static** dashboard and CSV artifacts for a simulated diagnostic stewardship pipeline.
It is designed to be published on **GitHub Pages** without a backend. Replace the CSV/PNG files with real pipeline
outputs to update the dashboard.

## Files
- `index.html` – Dashboard page referencing local PNG charts and CSV artifacts
- `diagnostic_tests_raw.csv`, `diagnostic_tests_processed.csv` – Raw and processed datasets
- `summary_by_department.csv` – Department-level classification distribution
- `monthly_non_actionable_rate.csv` – Non-actionable rate by month
- `data_quality_report.csv` – Latest data quality snapshot
- `pipeline_log.csv` – Run audit log
- `dept_classification_stacked.png`, `monthly_non_actionable_rate.png` – Matplotlib charts

## How to Publish on GitHub Pages
1. Create a new **public** GitHub repository (e.g., `diagnostic-stewardship-dashboard`).
2. Upload all files from this folder (`/diagnostic_dashboard`) into the repository root.
3. In your repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set:
   - **Source**: “Deploy from a branch”
   - **Branch**: `main` (or `master`) and **/ (root)** folder
5. Click **Save**. GitHub Pages will build the site. Your dashboard will be available at the URL shown on that page (usually `https://<username>.github.io/<repo>`).

## Local Development
- Open `index.html` in a browser to view the dashboard locally.
- To regenerate simulated data and charts, re-run the Python script that produced these files.

## Customization
- Update the logo URL inside `index.html` for your organization’s branding.
- Replace `*.csv` and `*.png` with production pipeline outputs (same filenames).
