# ice-wedge: Predicting Ice Nucleation in Wedge Geometries

**ice-WEDGE** is an open-source Python toolkit for predicting heterogeneous ice nucleation temperatures and critical nucleus geometry in wedge-shaped surface defects. Built on Classical Nucleation Theory (CNT) and the HINT algorithm, the tool leverages Gaussian Process Regression (GPR) to interpolate simulation data across wedge angles, depths, and surface binding strengths.

## Installation

To install and run `ice-WEDGE`, clone this repository:

```bash
git clone https://github.com/Molinero-Group/ice-wedge.git
cd ice-wedge
```

Install dependencies (create a new environment if needed):

```bash
conda create -n ice-wedge-env python=3.9
conda activate ice-wedge-env
pip install -r requirements.txt
```

## Repository Structure

```
ice-wedge/
├── data/                  # Precomputed simulation data
├── src/                   # Core scripts for Thet prediction
│   ├── model_fit.py       # GPR model training and prediction
│   ├── predict_thet.py    # Main CLI for nucleation temperature prediction
│   └── nucleus_geometry.py # Calculate nucleus size, contact angle, etc.
├── notebooks/             # Jupyter notebooks for examples and visualization
├── figures/               # Figures used in publication
├── LICENSE
├── README.md
└── requirements.txt       # Python dependencies
```

## Basic Usage

You can run the ice-WEDGE prediction tool from the command line:

```bash
python src/predict_thet.py --angle 70.5 --depth 5.0 --binding 0.66
```

### Arguments:

* `--angle`: wedge angle in degrees
* `--depth`: wedge depth in nanometers
* `--binding`: binding strength relative to ice (0–1 scale)

### Output:

Returns a prediction of:

* Heterogeneous nucleation temperature (Thet)
* Dominant barrier (ΔGin or ΔGout)
* Nucleus geometry (contact angle, radius, number of water molecules)

## Citation

If you use ice-WEDGE in your research, please cite:

Ribeiro, I. A.; Qiu, Y.; Metya, A. K.; Molinero, V. *Topographical Defects Can Confer Exceptional Ice Nucleation Ability to Mediocre Nucleants*, \[Journal], (2025).

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact

For questions or contributions, please contact:

**Valeria Molinero**
*Department of Chemistry, University of Utah*
[valeria.molinero@utah.edu](mailto:valeria.molinero@utah.edu)

---

**Developed by**: Ingrid de Almeida Ribeiro, Yuqing Qiu, Atanu K. Metya, and the Molinero Group

