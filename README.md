# ASK
## Aim:
To implement Amplitude Shift Keying (ASK) and observe its output waveform.

## Tools Required:
Python with NumPy & Matplotlib

Digital Signal Processor (DSP) (for hardware implementation)

Oscilloscope

Modulator & Demodulator

## Python Program for ASK Modulation:
import numpy as np

import matplotlib.pyplot as plt

fs = 1000

bit_rate = 1

t = np.arange(0, 10, 1/fs)

f_carrier = 5

data_bits = np.random.randint(0, 2, 10)

bit_signal = np.repeat(data_bits, fs // bit_rate)

carrier = np.sin(2 * np.pi * f_carrier * t)

ask_signal = carrier * bit_signal # Multiply carrier with binary signal

plt.figure(figsize=(12, 6))

plt.subplot(3, 1, 1)

plt.step(t, bit_signal, where='mid', color='black')

plt.ylim(-0.2, 1.2)

plt.title("Binary Input Signal")

plt.xlabel("Time [s]")

plt.ylabel("Amplitude")

plt.grid()

plt.subplot(3, 1, 2)

plt.plot(t, carrier, color='blue')

plt.title("Carrier Signal")

plt.xlabel("Time [s]")

plt.ylabel("Amplitude")

plt.grid()

plt.subplot(3, 1, 3)

plt.plot(t, ask_signal, color='red')

plt.title("ASK Modulated Signal")

plt.xlabel("Time [s]")

plt.ylabel("Amplitude")

plt.grid()

plt.tight_layout()

plt.show()

## output :
![graph digital](https://github.com/user-attachments/assets/33634506-4852-486e-a45e-437d93cd1e3b)


## Result :
The binary data was successfully modulated using Amplitude Shift Keying (ASK).

The ASK waveform was observed, where carrier presence represents '1' and absence represents '0'.

The experiment successfully demonstrated digital-to-analog conversion using ASK.
