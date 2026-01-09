# ice-wedge: Predicting Ice Nucleation in Wedge Geometries

**ice-WEDGE** is an open-source Python toolkit for predicting heterogeneous ice nucleation temperatures and critical nucleus geometry in wedge-shaped surface defects. Built on Classical Nucleation Theory (CNT) and the HINT algorithm, the tool uses Gaussian Process Regression (GPR) to interpolate CNT data across wedge angles, depths, and surface binding strengths.

## Requirements

Make sure you have the following Python packages installed:

`pip install numpy pandas matplotlib scipy scikit-learn openpyxl`

or

`conda install numpy pandas matplotlib scipy scikit-learn openpyxl`

## Inputs

CNT training data used to train the GPR model `data-GPR-model.xlsx`

Users can directly define the following parameters in the notebook:
- Wedge angle (eta) in degrees (between 20°–180°)
- Wedge depth (h) in nm
- Temperature of the flat surface $T_{flat}$ in K (used to determine the binding energy)
- Contact angle β of the outer surface
<br><br>
<img width="780" height="311" alt="image" src="https://github.com/user-attachments/assets/285075cc-e722-49d3-9ae9-72eb50dd5134" />

## How to Use

Open the notebook:

`jupyter notebook predict-wedgeHINT-GPR.ipynb`

Run each cell sequentially

- The notebook begins by setting up the data and computing $T_{flat}$ for various binding energies.
- It fits Gaussian Process models for different binding strengths.
- The user can input custom geometries to predict $T_{het}$ and assess which nucleation barrier dominates.

The Gaussian Process model is trained using a radial basis function (RBF) kernel and optimized to minimize prediction error across wedge geometries. 
The trained model is used to interpolate nucleation temperatures for arbitrary wedge angles and depths.

## Outputs

- $T_{het}$ predictions: Nucleation temperature within the wedge, and outside the wedge
- Shape of the critical nucleus inside the wedge
- The dominant barrier
- Plots: GPR fits and predicted nucleation temperatures vs. geometry

Example Output Screenshots

<table> <tr> <td align="center" width="50%" style="padding: 10px;"> <img width="423" height="322" alt="GPR results" src="https://github.com/user-attachments/assets/58d2a12e-ed2e-408c-8222-fe9aa40a4d71" /> <br/> <sub>Critical nucleus shape inside the wedge</sub> </td> <td align="center" width="50%" style="padding: 10px;"> <img width="436" height="296" alt="Thet as a function of geometry" src="https://github.com/user-attachments/assets/c3194efb-e66b-488e-b984-50b6f023c0aa" /> <br/> <sub>Thet as a function of geometry</sub> </td> </tr> <tr> <td align="center" width="50%" style="padding: 10px;"> <img width="599" height="300" alt="Critical nucleus shape" src="https://github.com/user-attachments/assets/2a4216c3-f82e-4937-bae6-7f33fd26a088" /> <br/> <sub>Thet inside and outside the wedge</sub> </td> <td align="center" width="50%" style="padding: 10px;"> <img width="988" height="540" alt="Barrier dominance map" src="https://github.com/user-attachments/assets/5fa14d49-e7f3-4420-8e8c-012cfb5e4efd" /> <br/> <sub>GPR plots</sub> </td> </tr> </table>

## Citation

If you use ice-WEDGE in your research, please cite:

Ribeiro, I. A.; Qiu, Y.; Gadea, E.; Metya, A. K.; Molinero, V. *Immersion Freezing at Topographic Active Sites: Dual-Barrier Prediction of Ice Nucleation Temperatures*, \[Journal], (2025).

The code and dataset are archived in Zenodo (DOI: 10.5281/zenodo.18201939). You are welcome to use and distribute this code as you see fit, but it remains the intellectual property of the authors and must be cited appropriately (please cite the paper). Direct any questions about this code to: Ingrid de A. Ribeiro (ingrid.ribeiro@utah.edu), or create an issue in this Github repository.

## Acknowledgement

I. de A. R and V. M. gratefully acknowledge support by AFOSR through MURI Award No. FA9550-20-1-0351.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.



