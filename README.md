#FM Using Python


<h3>Aim</h3>
To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

<h3>Apparatus Required</h3>
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

<h3>Theory</h3>

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:

<h3>Algorithm</h3>

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2. Generate Time Axis: Create a time vector for the signal duration.
3. Generate Message Signal: Define the message signal as a cosine wave.
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

#program
```
import numpy as np
import matplotlib.pyplot as plt
Am = 3.4
Ac = 6.8
fm = 940
fc = 9400
fs = 94000
t = np.arange(0, 2/fm, 1/fs)
B = 5.75
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
efm = Ac * np.cos(2 * np.pi * fc * t + B * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()
```

<h3>Output Waveform</h3>
<img width="1536" height="898" alt="Figure_3" src="https://github.com/user-attachments/assets/cc7738ef-3fc8-4d83-8c5f-45ce5150a9c9" />

<h3>Result</h3>
The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
