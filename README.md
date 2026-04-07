# Motor-Imagery-BCI-Classification
This repository contains a complete pipeline for decoding human motor intent from EEG signals. Developed by a multidisciplinary team of physicists and engineers, this project bridges the gap between raw neurophysiological data and actionable machine learning insights.

# Project Overview

The goal of this project is to classify whether a subject is imagining moving their hands or feet. This is a fundamental building block for:
Neuro-rehabilitation: Helping patients with motor impairments.
Industrial Safety: Monitoring cognitive states in high-risk environments.
BCI Gaming: Developing new paradigms for human-computer interaction.

# Technical Stack

Language: Python 3.11+
Signal Processing: MNE-Python (The gold standard for EEG/MEG data).
Machine Learning: Scikit-learn (CSP + LDA Pipeline).
Dataset: PhysioNet EEG Motor Movement/Imagery Database.

# Physics & Methodology

As physicists, we prioritized the Signal-to-Noise Ratio (SNR) and spatial localization:

- Preprocessing:
Temporal Filtering: Applied a Band-pass filter (8-14 Hz) to isolate the Mu (μ) Rhythm, the primary frequency band for motor cortex activity.

- Artifact Removal: Baseline correction and noise attenuation.

- Feature Extraction:
Used Common Spatial Patterns (CSP) to find optimal spatial filters that maximize the variance between classes.

- Classification:
Implemented Linear Discriminant Analysis (LDA) for robust and fast classification, ideal for potential real-time applications.

# Key Results
Accuracy: Achieved a peak cross-validation accuracy of ~67% (significantly above the 50% chance level for a binary task).
Spatial Localization: Topographic maps clearly show activation in the C3/C4 regions (Motor Cortex).
Artifacts (Visualizations)
topomap_c3.png: Shows the localized neural activity during imagery tasks.
confusion_matrix.png: Statistical breakdown of model performance.
eeg_signal_filter.png: Comparison between raw and processed signals.
