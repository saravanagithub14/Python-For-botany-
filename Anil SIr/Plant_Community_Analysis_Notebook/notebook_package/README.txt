Plant_Community_Analysis.ipynb — full pipeline in one notebook:
  0. Setup
  1. Load raw plot workbook -> tidy long format
  2. Alpha diversity (richness, Shannon, Simpson, Pielou) + Table 1 + Figures 1-2
  3. Community composition: PERMANOVA, PERMDISP, PCoA + Figure 4
  4. Species accumulation curves (sampling completeness) + Figure 3
  5. Save all outputs (CSVs, PNGs, results.txt)
  6. Notes on what's not yet covered (indicator species, constrained ordination, GLMMs — do in R)

To run on your real data:
  1. Replace mock_plant_survey_5_plots.xlsx with your actual workbook (same sheet layout: one
     sheet per plot, PLANT column + pre/monsoon/post-monsoon count columns, TOTAL row).
  2. Edit the INPUT_FILE and ZONE_MAP variables in the Setup cell (cell 2) to match your file name
     and real plot -> climate zone assignment.
  3. Kernel -> Restart & Run All.

Requirements: pandas, numpy, scipy, scikit-bio, matplotlib, seaborn, openpyxl
Install:  pip install pandas numpy scipy scikit-bio matplotlib seaborn openpyxl --break-system-packages
Run from the command line instead of Jupyter Lab:
  jupyter nbconvert --to notebook --execute --inplace Plant_Community_Analysis.ipynb
