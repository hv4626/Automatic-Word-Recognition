# Automatic-Word-Recognition
## Speech Command Recognition using Hidden Markov Models (HMM)

### Overview

This repository contains the code for Speech Command Recognition using Hidden Markov Models (HMM) as part of the assignment for the course EE679. The work has been done by Harshvardhan (20D070035).

**Key Features:**

* Implements speech command recognition using Hidden Markov Models (HMM)
* Preprocesses audio data, extracts features, trains HMM models, and makes predictions
* Employs Python libraries like librosa, matplotlib, numpy, hmmlearn, shutil, and sklearn
* Provides functions for extracting features, training HMM models, and evaluating performance

### Installation

Before running the code, ensure you have installed the required dependencies:

```bash
pip install librosa matplotlib numpy hmmlearn
```

### Definitions

The code includes several functions for specific tasks:

* `extract_and_set_permissions(zip_path, extract_path)`: Extracts files from a ZIP archive and sets permissions.
* `train_test_read(datapath, dataset_array)`: Reads and processes audio data for training and testing.
* `pre_emp(input, k)`: Applies pre-emphasis to the input signal.
* `end_pointing(sound_file, sampling_rate)`: Identifies endpoints in the audio signal.
* `mfcc(sound_file, sr)`: Computes Mel-Frequency Cepstral Coefficients (MFCC) features.
* `prediction(test_data, trained_model)`: Makes predictions using trained HMM models.
* `plot_confusion_matrix(cm, classes, title, filename)`: Plots and saves confusion matrices.

### Train-Test Process

The main code involves a train-test process with the following steps:

**Training:**

1. Reads and processes training data.
2. Applies endpointing, pre-emphasis, and computes MFCC features.
3. Trains Gaussian HMM models for each word.

**Testing:**

1. Reads and processes clean and noisy test datasets.
2. Applies endpointing, pre-emphasis, and computes MFCC features.
3. Makes predictions using trained HMM models.

**Evaluation:**

1. Computes confusion matrices for clean and noisy test datasets.
2. Plots and saves confusion matrices.

### Usage

Adjust file paths and parameters as needed for your dataset.

### Results

The code outputs confusion matrices for both clean and noisy test datasets. These matrices can be used to evaluate the performance of the speech command recognition system.
