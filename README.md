# QPSK Wireless Communication Link Simulation in MATLAB

## Overview

This project presents a MATLAB-based simulation of a Quadrature Phase Shift Keying (QPSK) digital communication link operating over an Additive White Gaussian Noise (AWGN) channel. The simulation examines how varying noise levels affect signal quality and communication reliability.

The system generates random binary data, performs Gray-coded QPSK modulation, applies Root Raised Cosine (RRC) pulse shaping, transmits the signal through an AWGN channel, and recovers the transmitted information using matched filtering and QPSK demodulation. System performance is evaluated using Bit Error Rate (BER) and constellation diagrams.

## Objectives

- Simulate a complete QPSK digital communication link in MATLAB.
- Study the effect of AWGN on transmitted QPSK signals.
- Evaluate system performance across different Eb/No values.
- Analyze the relationship between channel noise and Bit Error Rate.
- Visualize signal distortion using constellation diagrams.
- Demonstrate the role of pulse shaping and matched filtering in digital communication.

## System Workflow

```text
Random Bit Generation
        |
        v
QPSK Modulation
        |
        v
RRC Pulse Shaping
        |
        v
AWGN Channel
        |
        v
Matched RRC Filtering
        |
        v
Symbol Recovery
        |
        v
QPSK Demodulation
        |
        v
BER and Constellation Analysis
```

## Key Features

- Random binary data generation
- Gray-coded QPSK modulation and demodulation
- Root Raised Cosine pulse shaping
- Oversampled signal transmission
- AWGN channel modeling
- Matched filtering at the receiver
- Filter-delay compensation
- BER calculation over multiple Eb/No values
- Constellation visualization under different noise conditions

## Simulation Parameters

| Parameter | Value |
|---|---|
| Modulation Scheme | QPSK |
| Modulation Order | 4 |
| Number of Symbols | 2000 |
| Bits per Symbol | 2 |
| Samples per Symbol | 8 |
| RRC Roll-off Factor | 0.25 |
| Filter Span | 6 symbols |
| BER Analysis Range | 0 to 6 dB Eb/No |
| Moderate-Noise Constellation | 4 dB |
| Low-Noise Constellation | 20 dB |
| High-Noise Constellation | 0 dB |

## Performance Analysis

The simulation evaluates the communication link by measuring the Bit Error Rate at different Eb/No values. As Eb/No increases, the influence of channel noise decreases, allowing the receiver to recover the transmitted bits more accurately.

The constellation diagrams provide a visual representation of the same behavior:

- **Low noise:** QPSK symbols form tight and clearly separated clusters.
- **Moderate noise:** The symbol clusters remain identifiable but show noticeable spreading.
- **High noise:** The received symbols become widely scattered, increasing the probability of incorrect symbol decisions.

## Requirements

- MATLAB
- Communications Toolbox

The project uses MATLAB functions and objects including `pskmod`, `pskdemod`, `rcosdesign`, `upfirdn`, and `comm.AWGNChannel`.

## Running the Simulation

1. Clone or download this repository.
2. Open MATLAB.
3. Navigate to the `src` directory.
4. Open `qpsk_link_robust.m`.
5. Run the script.

The program generates:

- BER versus Eb/No plot
- QPSK constellation at moderate noise
- Low-noise QPSK constellation
- High-noise QPSK constellation
- BER values in the MATLAB Command Window

## Repository Structure

```text
qpsk-wireless-communication-matlab/
|
|-- src/
|   |-- qpsk_link_robust.m
|
|-- LICENSE
|-- README.md
```

## Future Improvements

Possible extensions of this project include:

- Comparison of simulated BER with theoretical QPSK performance.
- Evaluation of other modulation schemes such as BPSK, 8-PSK, and QAM.
- Simulation under Rayleigh and Rician fading channels.
- Implementation of channel coding techniques.
- Extension to a hardware-based Software-Defined Radio platform.

## Author

**Vaidya Sharanya**  
Electronics and Communication Engineering  
BVRIT Hyderabad College of Engineering for Women

## License

This project is available under the MIT License.
