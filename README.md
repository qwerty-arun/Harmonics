# Audio Harmonic Synthesis and Filtering with libSoX: A Comparison Study

## Objective
To synthesize periodic waveforms using sine harmonics, apply digital filters using SoX's built-in tools (low-pass, high-pass), and compare the output to filters provided in Audacity based on frequency content.

## Tools Used
- **Bash + SoX (libSoX):** waveform generation, filtering, spectrograms
- **Audacity:** secondary filter tool and spectrum analyzer
- **Spectrogram Analysis:** via SoX and Audacity

## Methodology

### 1. Waveform Synthesis
- Square, sawtooth, and triangular waves were constructed using multiple `sox` commands summing harmonics.
- Harmonic weights were adjusted per Fourier synthesis rules.

### 2. Filtering
- SoX's `lowpass` and `highpass` effects were used to isolate or suppress harmonics.
- These filters are based on IIR approximations (like Butterworth).

### 3. Spectral Analysis
- Frequency content before and after filtering was visualized via SoX’s spectrogram and Audacity's frequency analysis.

## Results
- **Low-pass filters** significantly reduced higher-order harmonics, smoothing the waveforms.
- **High-pass filters** removed low frequencies, keeping sharp edges and high-frequency components.
- **Audacity's filters** produced nearly identical results, confirming the effectiveness of SoX’s built-in filter algorithms.

## Conclusion
- SoX’s built-in `lowpass` and `highpass` filters perform comparably to Audacity’s.
- There was no substantial spectral difference in the output between both tools.
- SoX provides a powerful scripting-based audio processing pipeline.

## Future Work
- Explore band-pass and band-reject filters.
- Automate full waveform + filter pipeline in one shell script.
- Compare phase responses using a signal analysis tool like MATLAB or Python.
