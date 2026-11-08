# Neurological_Voice_Analysis-Acoustic Speech Analysis Prototype

## 1. Motivation

The idea for this project emerged after my grandmother was diagnosed with Parkinson's disease.

While observing changes in her speech, I noticed something that made me curious: although her sentence structures and the overall content of her speech remained largely familiar, the way she sounded seemed different. Her voice became quieter, her intonation changed, and her usual manner of speaking gradually began to sound different.

I started wondering whether such changes, which can be perceived by human hearing but are difficult to describe precisely, could be measured objectively.

This observation led me to the following question:

**Can computational methods be used to identify changes in the acoustic characteristics of speech, even when its linguistic content remains largely unchanged?**

I also became interested in whether certain acoustic changes could be associated with neurological conditions.

## 2. Project Overview

Voice Analysis is an experimental project focused on developing a prototype for acoustic speech analysis using digital signal processing and machine learning.

The main idea is to transform voice recordings into numerical data, analyze their acoustic characteristics, and investigate how these characteristics vary.

Unlike systems primarily focused on speech recognition and linguistic meaning, this project focuses on **how speech sounds**.

The long-term objective is to explore whether consistent acoustic changes can be identified and whether they may be associated with neurological conditions.

This project is currently an early-stage prototype and is not a completed diagnostic system.

## 3. Technical Approach

The proposed analysis pipeline consists of several stages:

1. Loading and preprocessing audio recordings.
2. Extracting acoustic features.
3. Converting speech characteristics into numerical representations.
4. Analyzing relationships and variability between acoustic features.
5. Exploring machine-learning methods for identifying recurring structures and changes.

### Acoustic Features

**Temporal and voice-related features:**

- **Fundamental Frequency (F0)** — the fundamental frequency of the voice.
- **RMS Energy** — a measure of the signal's energy, related to its intensity.
- **Speech Tempo** — speaking rate.
- **Pauses** — duration and distribution of pauses.
- **Pitch Variability** — variation in fundamental frequency.
- **Jitter** — cycle-to-cycle variations in vocal fold vibration period.
- **Shimmer** — cycle-to-cycle variations in vocal amplitude.

**Spectral features:**

- **Spectral Centroid** — the center of mass of the spectral energy distribution.
- **Spectral Bandwidth** — the spread of spectral energy around the centroid.
- **Spectral Rolloff** — the frequency below which a specified proportion of spectral energy is concentrated.
- **MFCC (Mel-Frequency Cepstral Coefficients)** — coefficients representing the spectral envelope of an audio signal.

Age, sex, and body weight were also considered as potential auxiliary variables that may influence individual voice characteristics.

## 4. Prototype Development

The initial prototype is being developed in Python using Google Colab.

### Implemented Components

The initial audio preprocessing stage includes:

- Audio file loading and validation.
- Conversion of audio recordings to mono format.
- Resampling to 22,050 Hz.
- Initial audio processing configuration.
- Extraction of recording duration.

### Preliminary Neural Network Architecture

I also explored a preliminary neural network architecture designed to process numerical speech features.

The experimental model uses four input features:

- Speech tempo.
- Pause ratio.
- Average pitch.
- RMS energy.

The proposed architecture consists of:

- Input layer with four features.
- First Dense layer — 32 neurons, ReLU activation.
- Second Dense layer — 16 neurons, ReLU activation.
- Output layer — 1 neuron, Sigmoid activation.

This architecture represents an initial machine-learning experiment and has not yet been established as the final model for the main project.

## 5. Technologies Used

- **Python** — primary programming language.
- **Google Colab** — development and experimentation environment.
- **Librosa** — audio loading and signal processing.
- **NumPy** — numerical computations and array operations.
- **TensorFlow / Keras** — neural network architecture exploration.

Additional Python standard modules used in the initial notebook include `json`, `argparse`, `pathlib`, and `warnings`.

## 6. Current Limitations

The project is currently in the early prototype development stage.

One of the main challenges is obtaining suitable audio datasets for model training and evaluation.

Further development requires speech recordings with reliable metadata and, where possible, relevant clinical information.

Repeated recordings of the same participants with temporal annotations would be particularly valuable, as they would allow the investigation of acoustic changes within individuals over time.

Without suitable data, it is not yet possible to reliably train and evaluate a model or establish whether detected acoustic changes are associated with specific neurological conditions.

Additionally, acoustic characteristics can be influenced by age, individual voice differences, emotional state, fatigue, and recording conditions. These factors must be considered in future experiments.

## 7. Future Development

Planned development includes:

- Completing the acoustic feature extraction pipeline.
- Exploring temporal and spectral representations of speech.
- Finding and obtaining suitable research datasets.
- Investigating natural variability in human speech.
- Developing methods for quantitatively analyzing acoustic changes.
- Comparing statistical methods and machine-learning approaches.
- Training and evaluating a model using appropriate data.

The long-term objective is to investigate whether computational speech analysis can provide additional objective information relevant to neurological research.

The system is intended as a supplementary analytical tool, not as a replacement for medical examinations or professional clinical judgment.

---

**Project Status:** Early Prototype Development
