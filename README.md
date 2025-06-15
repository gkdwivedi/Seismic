# Well Top to Surface Depth Comparison Tool

This Python script performs **4-point nearest-neighbor interpolation** to estimate surface depth at well top locations. It is designed for geoscientists working with tops and surface data (in depth, feet) to calculate differences between well top depths and interpolated surface depths.

---

## Functionality

For each well top in the input file:

1. Identifies the corresponding surface file from the `surfaces/` folder.
2. Locates the `(X, Y)` coordinate from the tops file.
3. Finds the 4 nearest points in the corresponding surface file.
4. Calculates the average surface depth from these 4 points.
5. Computes the difference between well top depth and interpolated surface depth.
6. Saves the final results to a CSV file.

---

## Folder Structure

project_folder/
│
├── tops_data.xlsx # Excel file with well tops
├── surfaces/ # Folder with surface CSV files
│ ├── LS3.csv
│ ├── MIRADOR.csv
│ └── ... (named after surface tops)
│
├── well_top_surface_comparison.csv # Output file (generated)
└── interpolate_tops.py # This script
