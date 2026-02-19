# Docking_Analysis_Suite - Python Tools for Molecular Docking Data Analysis

[![DOI](https://zenodo.org/badge/1162006212.svg)](https://doi.org/10.5281/zenodo.18704239)

A collection of Python scripts for visualizing and analyzing protein-ligand molecular docking results. This repository provides tools to generate publication-quality figures from docking score data, enabling quick assessment of binding affinities and structure-activity relationships.

The script was written and developed by Leonardo Broetto (leonardo.broetto@arapiraca.ufal.br, Lbroetto@gmail.com)

# Contact
**Authors:** Leonardo Broetto
**Correspondence:** Lbroetto@gmail.com, leonardo.broetto@arapiraca.ufal.br
**Affiliation:** Núcleo de Pesquisa em Bioinformática e Filogenômica (NPBF - Bioinformatics and Phylogenomics Research Group), Universidade Federal de Alagoas, Brasil (Federal University of Alagoas, Brazil)

## Repository Structure

| Directory/File | Description |
|----------------|-------------|
| `Docking_heatmap.py ` | Heatmap generator for energy scores |
| `Docking_relplot_ligand.py` | Scatter plot colored by ligand |
| `Docking_relplot_protein.py` | Scatter plot colored by protein |
| `LICENSE` | GNU GPLv3 license |
| `README.md` | This documentation |

## Scripts Overview
- Docking_heatmap.py. Generates an annotated heatmap visualization of docking energy scores, ideal for comparing binding affinities across multiple protein-ligand combinations.

Mathematical basis: The heatmap uses a color gradient to represent binding energy values (ΔG in kcal/mol). Lower (more negative) scores indicate stronger binding affinity. The visualization follows the thermodynamic principle that more favorable binding corresponds to more negative free energy values.

- Docking_relplot_ligand.py. Creates a scatter plot exploring the relationship between docking energy scores and hydrogen bond formation, with data points colored by ligand identity.

Scientific rationale: This plot helps identify whether stronger binding (more negative energy) correlates with increased hydrogen bonding, and whether different ligands show distinct patterns in this relationship.

- Docking_relplot_protein.py. Similar to the ligand version, but colors data points by protein target, enabling comparison of binding patterns across different receptors.

Statistical approach: The scatter plots facilitate visual identification of:

Linear or non-linear relationships between energy and hydrogen bonds

Clustering patterns by protein/ligand

Outliers or exceptional binding cases

### Scripts Summary

| Script | Purpose | Required CSV Columns | Output Figure |
|--------|---------|---------------------|---------------|
| `Docking_heatmap.py` | Generate binding energy heatmap | `Protein`, `Ligand`, `Energy_Score` | `docking_energy_heatmap.png` |
| `Docking_relplot_ligand.py` | Energy vs H-bonds scatter (colored by ligand) | `Ligand`, `Energy_Score(kcal/mol)`, `Hydrogen_Bonds` | `energy_vs_hbonds_by_ligand.png` |
| `Docking_relplot_protein.py` | Energy vs H-bonds scatter (colored by protein) | `Protein`, `Energy_Score(kcal/mol)`, `Hydrogen_Bonds` | `energy_vs_hbonds_by_protein.png` |

----
# Quick Start: Using the Scripts
Before running a script:

Prepare your data: Prepare your data in CSV format with the required columns (see table above)

Configure the script: Open the script file and locate the INPUT_FILE variable at the top. Change its value to match your CSV filename.

Install dependencies: Ensure you have the required Python packages installed (see Requirements).

Run the script: Execute it from your terminal or IDE: python script_name.py

Data Privacy Note: The original research data is not included in this repository. The script is configured to work with generic filenames (input_data_table.csv). Replace this with your own data filename.

Expected Data Location: By default, script look for the CSV file in the same directory as the script. You can modify the path in the INPUT_FILE variable if needed (e.g., 'data/my_file.csv').

### For Reproducibility and Reuse:
1.  **Code Execution:** To run this script with your own data, simply place your CSV file in the `data/` directory and update the filename in the script (or rename your file to match the expected name in the script).
2.  **Data Format:** script includes a comment at the top describing the **required input** and **configuration** for the input CSV. Please ensure your data follows this format.

## Requirements & Installation

### Python Dependencies
Create a conda environment or install directly:
``bash
pip install pandas numpy matplotlib seaborn

## Versions Tested
Python 3.8+
pandas 1.3.0
seaborn 0.11.0
matplotlib 3.3.0

# License and Citation

### If you use this analysis script in your research, please cite:

Broetto, L. (2026). Python Tools for Molecular Docking Data Analysis (v1.0.0) [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.18704240

or

```bibtex
@software{broetto_Docking_Analysis_Suite_2026,
  author       = {Leonardo Broetto},
  title        = {{Python Tools for Molecular Docking Data Analysis}},
  month        = jan,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.18704240},
  url          = {https://doi.org/10.5281/zenodo.18704240}
}
```

This project is licensed under the **GNU General Public License v3.0**.

### Terms for Academic/Research Use:
- Free to use, study, and modify
- Must distribute derivatives under GPLv3
- Must provide source code when distributing binaries
- Must preserve copyright notices and license text

### Terms for Commercial Use:
For commercial applications or proprietary integration, please contact the author (Lbroetto@gmail.com, leonardo.broetto@arapiraca.ufal.br) to discuss alternative licensing options.

**Full license text:** [LICENSE](LICENSE)

## Intellectual Property Notice

The computational methods, algorithms, and models implemented in this software are research outcomes from Universidade Federal de Alagoas. While the source code is licensed under GPLv3 for academic and open-source use, commercial licensing options are available.

This software is available under two licenses:
1. GNU GPLv3 for open source/academic use
2. Commercial license for proprietary use (contact author)
For commercial licensing, technology transfer, or collaboration inquiries:
Contact: Lbroetto@gmail.com, leonardo.broetto@arapiraca.ufal.br


### Copyright and Licensing
- **Copyright Holder:** Leonardo Broetto 
- **License:** GNU General Public License v3.0
- **Year:** 2026

### Research Attribution
The computational methodologies implemented in this software were developed as part of research activities conducted by Leonardo Broetto. Associated research work is linked to Universidade Federal de Alagoas.

### Usage Terms
- **Academic/Research Use:** Permitted under GPLv3 with mandatory citation
- **Commercial Use:** Requires alternative licensing (contact author)
- **Derivative Works:** Must be released under GPLv3

### Contact for Licensing
Leonardo Broetto
Lbroetto@gmail.com, leonardo.broetto@arapiraca.ufal.br
(Associated with Universidade Federal de Alagoas)

