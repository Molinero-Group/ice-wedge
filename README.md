# ice-wedge: Predicting Ice Nucleation in Wedge Geometries

**ice-WEDGE** is an open-source Python toolkit for predicting heterogeneous ice nucleation temperatures and critical nucleus geometry in wedge-shaped surface defects. Built on Classical Nucleation Theory (CNT) and the HINT algorithm, the tool uses Gaussian Process Regression (GPR) to interpolate CNT data across wedge angles, depths, and surface binding strengths.

## Requirements

Make sure you have the following Python packages installed:

`pip install numpy pandas matplotlib scipy scikit-learn`

or

`conda install numpy pandas matplotlib scipy scikit-learn`

## Inputs

CNT training data used to train the GPR model `data-GPR-model.xlsx`

Users can directly define the following parameters in the notebook:
- Wedge angle (eta) in degrees (between 20°–180°)
- Wedge depth (h) in nm
- Temperature of the flat surface $T_{flat}$ in K (used to determine the binding energy)

## How to Use

Open the notebook:

`jupyter notebook predict-wedgeHINT-GPR.ipynb`

Run each cell sequentially:

- The notebook begins by setting up the data and computing $T_{flat}$ for various binding energies.
- It fits Gaussian Process models for different binding strengths.
- The user can input custom geometries to predict $T_{het}$ and assess which nucleation barrier dominates.

## Outputs

- $T_{het}$ predictions: Nucleation temperature within the wedge, and outside the wedge
- Shape of the critical nucleus inside the wedge
- The dominant barrier
- Plots: GPR fits

## Citation

If you use ice-WEDGE in your research, please cite:

Ribeiro, I. A.; Qiu, Y.; Gadea, E.; Metya, A. K.; Molinero, V. *Topographic Defects Control Ice Nucleation Temperatures through a Dual-Barrier Mechanism*, \[Journal], (2025).

You are welcome to use and distribute this code as you see fit, but it remains the intellectual property of the authors and must be cited appropriately (please cite the paper). Direct any questions about this code to: Ingrid de A. Ribeiro (ingrid.ribeiro@utah.edu), or create an issue in this Github repository.

## Acknowledgement

I. de A. R and V. M. gratefully acknowledge support by AFOSR through MURI Award No. FA9550-20-1-0351.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.



