# Exo-planet_Detect

This project implements a deep learning model using CNNs to detect the presence of **transiting exoplanets** based on planetary system data. Inspired by the Kepler mission and NASA's light curve analysis, this model learns to identify patterns that indicate a planet transit.

---

##  Project Goal

Build a supervised classification model that predicts **whether a planet transits its star** (i.e., is detectable via transit method), using a set of orbital and physical parameters of exoplanets.

---

##  Model Architecture

- **Model Type**: Convolutional Neural Network (CNN)
- **Input**: Structured planetary system data or engineered light curve–like features
- **Output**: Binary class (Planet Detected / Not Detected)
- **Performance**: ~99% accuracy on test data

---

##  Features Used

Typical features used in the dataset:
- `pl_orbper`: Orbital period
- `pl_ratror`: Planet/star radius ratio
- `pl_ratdor`: Semi-major axis to stellar radius
- `pl_bmassj`: Planetary mass
- `pl_orbeccen`: Eccentricity
- `st_rad`, `st_teff`: Stellar radius and temperature
- (Optional) Light curve pattern or derived photometric features

> Label: `has_transit` (1 if a transit is detected, 0 otherwise)

---

##  File Structure

- `cnn_exoplanet_detection.ipynb` – Training notebook
- `data/` – Planetary dataset (CSV from NASA Exoplanet Archive)
- `model/` – Saved weights and model checkpoints
- `plots/` – Accuracy, loss, confusion matrix, etc.
- `requirements.txt` – Required Python packages
