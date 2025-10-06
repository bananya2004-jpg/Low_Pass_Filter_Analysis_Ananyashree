🎚️ Low Pass Filter Analysis — B Ananyashree
📘 Assignment Overview

This repository documents the analysis of a Low Pass Filter (LPF) circuit using the Digilent WaveForms tools.
The goal is to experimentally verify the frequency response of an RC low-pass filter by varying the input signal frequency and measuring the corresponding output amplitude.

🗂️ Repository Structure
low-pass-filter-analysis-ananyashree/
│
├── data
│   └── data_measurements.csv               # Recorded measurements and calculated gain
│
├── images
│   ├── WaveForms_Lab_Assignment_2a   # The doc contains all the related images and plot│   
│ 
├── scripts
│   └── default.wf            # Script in waveforms used to generate sine wave
│
└── README.md                      # Assignment documentation

🎯 Assignment Objectives
To study and analyze the frequency response of an RC Low Pass Filter.
To observe the attenuation behavior beyond the cutoff frequency (1 kHz).
To calculate the gain in decibels (dB) for multiple frequencies.
To verify that the filter allows low frequencies to pass and attenuates higher frequencies.
⚙️ Experimental Steps

Part 1: Signal Generation
Used the Wavegen tool in Digilent WaveForms to generate sinusoidal signals at:
100 Hz, 500 Hz, 1 kHz, 2 kHz, 5 kHz, and 10 kHz.
Maintained a fixed input voltage amplitude throughout all tests.

Part 2: Measurement
Connected the RC low-pass filter output to the Scope tool.
Measured output voltage amplitude (Vout) for each frequency.
Recorded both Vin and Vout values.

Part 3: Gain Calculation
Computed gain for each test frequency using:
Gain (dB) = 20 × log10(Vout / Vin)

Created a table summarizing frequency, Vout, and calculated gain.
Part 4: Visualization
Used Excel to plot: Gain (dB) vs Frequency (Hz)
<img width="685" height="204" alt="image" src="https://github.com/user-attachments/assets/efb40f8a-1ce3-4943-b329-9f6f5e185eb9" />
<img width="752" height="452" alt="image" src="https://github.com/user-attachments/assets/8e1e6aea-88b1-4dd3-afae-3b19a962dadd" />

Frequency axis displayed on a logarithmic scale.
Part 5: Observations
Plotted responses confirm low attenuation below 1 kHz and rapid attenuation above it.
The cutoff frequency (fc) was approximately 1 kHz, as expected for the RC values used.
For frequencies below fc, the output closely follows the input (gain ≈ 0 dB).
For frequencies above fc, output amplitude decreases rapidly.
The -3 dB point around 1 kHz marks the boundary between the passband and stopband.
The experimental curve matches the theoretical low-pass response.

Part 6: Formula Reference
$$
f_{c} = \frac{1}{2\pi R C}
$$

$$
\mathrm{Gain\ (dB)} = 20 \log_{10}\!\left(\frac{V_{\text{out}}}{V_{\text{in}}}\right)
$$

✅ Outcome
The practical experiment successfully demonstrated the frequency-dependent behavior of an RC Low Pass Filter.
The observed gain vs frequency response validates the theoretical design, confirming the filter’s ability to attenuate high-frequency components above the cutoff frequency.

