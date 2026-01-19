# Data-Augmentation-Techniques-for-Children-s-Automatic-Speech-Recognition-ASR-
The project focuses on applying and evaluating audio data augmentation techniques to improve the robustness and generalization of Children’s Automatic Speech Recognition (ASR) systems.
Children’s speech presents unique challenges such as high pitch variability, pronunciation inconsistency, and limited labeled data. Data augmentation is a key strategy to mitigate data scarcity and improve ASR performance in such scenarios.


## Dataset

- Children’s speech audio samples (e.g., CMU Kids / ESPnet-based child ASR corpora).

- Audio files are processed at their original sampling rates to avoid distortion.

- Augmented audio samples are saved and listed for downstream ASR training.

## Tools & Libraries Used

- Python

- Librosa – audio loading and signal processing

- SpeechBrain – ASR-focused augmentation utilities

- nlpaug – audio data augmentation

- NumPy

- SoundFile

## Techniques Implemented

### 1. Time Shifting

Circularly shifts the waveform in the time domain.

Simulates speaking rate and alignment variations.

Implemented using NumPy array rolling.

### 2. Loudness / Volume Perturbation

Alters signal amplitude to simulate different speaking intensities and microphone distances.

Helps models become invariant to volume changes.

### 3. Random Cropping

Randomly removes or crops segments of the speech signal.

Encourages robustness against partial or truncated utterances.

Implemented using nlpaug audio augmenters.

### 4. Frequency Masking / Drop Frequency

Randomly removes certain frequency bands.

Simulates channel distortion and environmental effects.

Used for realistic and ASR-compatible data perturbations.
