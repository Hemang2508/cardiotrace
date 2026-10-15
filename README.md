# CardioTrace
[![DOI](https://zenodo.org/badge/1420285431.svg)](https://doi.org/10.5281/zenodo.23387336)

**A web-based ECG simulator for fifteen cardiac rhythms, built on a parametric Gaussian model.**

Live demo: https://eloquent-crisp-493f47.netlify.app/

CardioTrace generates synthetic electrocardiogram (ECG) waveforms on demand for ECG education, algorithm testing, and synthetic data generation. No patient records are used or stored. Every waveform is computed in the browser from model parameters.

## How it works

Each ECG component (the P wave, the QRS complex and the T wave) is modelled as a Gaussian basis function with three parameters: amplitude, temporal position and width. Each cardiac condition is produced by modifying these parameters to reproduce its characteristic diagnostic features.

Signals are generated through a seven-stage pipeline:

1. Parameter initialisation
2. Gaussian wave synthesis
3. Beat template construction
4. Multi-beat assembly with rhythm-specific RR-interval modelling
5. Waveform modification
6. Additive noise injection
7. Rendering with diagnostic parameter display

## Conditions covered

The fifteen simulated rhythms span normal sinus rhythm, rate abnormalities, atrial arrhythmias, atrioventricular conduction disorders, ischaemic syndromes, ventricular arrhythmias, bundle branch blocks, repolarisation abnormalities and accessory pathway syndromes.

## Running locally

CardioTrace is plain HTML, CSS and JavaScript with no build step.

```bash
git clone https://github.com/Hemang2508/cardiotrace.git
cd cardiotrace
```

Then open `index.html` in any modern browser.

## Associated paper

This repository accompanies the paper *ECG Simulator for Cardiac Rhythm Visualisation and Educational Applications* (IEEE conference submission, under review). Citation details will be added on publication.

## Citing this software

   If you use CardioTrace, please cite the archived release on Zenodo: https://doi.org/10.5281/zenodo.23387337. Citation metadata is also available in `CITATION.cff`.

## License

Released under the MIT License. See `LICENSE`.
