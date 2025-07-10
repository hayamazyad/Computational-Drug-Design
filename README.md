# Molecule Visualizer with Topological Indices
This interactive Jupyter Notebook allows users to visualize molecular structures from .mol and .sdf files and compute graph-based topological indices. It’s designed to support basic cheminformatics tasks and educational exploration of molecular graph theory.

<div align="right" style="font-size:16px; color:black; font-family:Segoe UI, sans-serif;">
Developed by Haya Mazyad & Lynn Oueidat
</div>

---
# Overview
This notebook calculates three important topological indices from molecular files:
- **Edge Density**: The ratio of actual edges to the maximum possible in the graph.
- **Wiener Index**: The sum of shortest path lengths between all non-hydrogen pairs of vertices.
- **Petitjean Index**: A normalized measure of asymmetry based on diameter and radius.

It also provides interactive molecule graph visualization with atom-level tooltips, hydrogen exclusion option, and navigation between multiple molecules.

---
# Supported Input Formats
The tool supports the following file types:
- A single .mol file 
- A single .sdf file containing one or more molecules
- A folder of .mol files
- A folder of .sdf files

---
# How It Works
1. Upload a .mol or .sdf file or folder (through path or browsing).
2. The notebook:
    - Parses the molecule(s) manually (no RDKit used)
    - Converts each into a graph using NetworkX
    - Computes the selected topological indices
    - Displays an interactive molecular graph using Plotly
3. Use Previous and Next buttons to browse molecules.
4. Tooltips show atom info: element, index, and 3D coordinates.
5. Optionally, export graphs as PNG images.

---
# Project Structure
This project contains:
  - MoleculeVisualizer.ipynb → Main Jupyter Notebook with all code and interactive widgets.
  - molecules/ → Folder where sample input .mol and .sdf files and folders are placed for testing.
  - output_images/ → Folder where exported PNGs will be saved (if enabled).
