# ice-wedge: Predicting Ice Nucleation in Wedge Geometries

**ice-WEDGE** is an open-source Python toolkit for predicting heterogeneous ice nucleation temperatures and critical nucleus geometry in wedge-shaped surface defects. Built on Classical Nucleation Theory (CNT) and the HINT algorithm, the tool leverages Gaussian Process Regression (GPR) to interpolate simulation data across wedge angles, depths, and surface binding strengths.

## Requirements

Make sure you have the following Python packages installed:

pip install numpy pandas matplotlib scipy scikit-learn openpyxl

## Output:

Returns a prediction of:

* Heterogeneous nucleation temperature (Thet)
* Dominant barrier (ΔGin or ΔGout)
* Nucleus geometry (contact angle, radius, number of water molecules)

## Citation

If you use ice-WEDGE in your research, please cite:

Ribeiro, I. A.; Qiu, Y.; Metya, A. K.; Molinero, V. *Topographical Defects Can Confer Exceptional Ice Nucleation Ability to Mediocre Nucleants*, \[Journal], (2025).

## Acknowledgement

I. de A. R and V. M. gratefully acknowledge support by AFOSR through MURI Award No. FA9550-20-1-0351.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.



