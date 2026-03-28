# 🧬 DSSP Secondary Structure Plotting (GROMACS / MD Analysis)

This repository provides a **Python + Google Colab workflow** to generate high-quality **DSSP secondary structure plots** from molecular dynamics simulations.

It is designed for researchers working with **protein dynamics, drug binding studies, and structural stability analysis**.

---

## 📌 Features

* ✅ Supports DSSP output from GROMACS
* ✅ Converts DSSP text data into publication-quality plots
* ✅ Handles large trajectory data efficiently
* ✅ Custom color scheme (Coil, Helix, Sheet, Turn, Bend)
* ✅ Single and multi-panel plotting supported
* ✅ Google Colab compatible (no installation required)

---

## 📂 Input Requirements

The script expects a DSSP text file (`.txt`) with the following format:

```
~EEEEEEE~TTS~HHHHHHHHH...
~EEEEEEE~TTS~HHHHHHHHH...
```

* Each line = one simulation frame
* Each character = secondary structure of a residue

---

## 🔬 DSSP Structure Mapping

| Symbol | Structure |
| ------ | --------- |
| H      | α-Helix   |
| G      | 3₁₀-Helix |
| I      | π-Helix   |
| E      | β-Strand  |
| B      | β-Bridge  |
| T      | Turn      |
| S      | Bend      |
| ~ / =  | Coil      |

---

## 🎨 Color Scheme

| Structure | Color        |
| --------- | ------------ |
| Coil      | Red          |
| β-Sheet   | Cyan-green   |
| Bend      | Blue         |
| Turn      | Yellow-green |
| α-Helix   | Teal         |
| 3₁₀-Helix | Bright green |

---

## 🚀 Usage (Google Colab)

### 1. Upload your DSSP file

```python
from google.colab import files
uploaded = files.upload()
```

---

### 2. Run the plotting script

The script will:

* Read DSSP data
* Convert to numerical matrix
* Generate a heatmap

---

### 3. Output

* 📊 DSSP heatmap (`.png`)
* X-axis → Time (ns)
* Y-axis → Residue number

---

## ⚙️ Workflow (MD Simulation)

Typical workflow using GROMACS:

```
traj.xtc
   ↓
gmx do_dssp
   ↓
ss.xpm
   ↓
Convert → dssp.txt
   ↓
Run this script → DSSP plot
```

---

## 📊 Output Interpretation

* Horizontal bands → stable secondary structures
* Disruptions → unfolding or ligand effects
* Comparison between systems → structural changes due to binding

---

## 🧠 Applications

* Protein folding analysis
* Drug-protein interaction studies
* Stability comparison (apo vs holo)
* Secondary structure evolution over time

---

## 🛠️ Dependencies

* Python 3.x
* NumPy
* Matplotlib

(Pre-installed in Google Colab)

---

## 🔥 Future Improvements

* ⏱ Time auto-detection from trajectory
* 📊 DSSP percentage plots
* 📈 Integration with RMSD / PCA analysis
* 🎯 Highlight binding site residues

---

## 👨‍🔬 Author

**Rajesh S.**
M.Sc. Biochemistry
Research focus: Molecular modeling, drug design, nano-biotechnology

---

## 📜 License

This project is open-source and available under the MIT License.

---

## ⭐ Acknowledgement

If you use this workflow in your research, please consider citing relevant DSSP and MD simulation tools.

---
