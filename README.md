# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt

am = 4.9
fm = 356
ac = 9.8
fc = 3560
fs = 35600
beta = 5.2
t = np.arange(0, 2/fm, 1/fs)

m = am * np.cos(2 * np.pi * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)

c = ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)

efm = ac * np.cos(2 * np.pi * fc * t + beta * np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,3)
plt.plot(t, efm)
plt.title("FM")

plt.tight_layout()
plt.show()
```


Output Waveform

![WhatsApp Image 2025-11-16 at 20 02 30_66b68bc1](https://github.com/user-attachments/assets/91dd5edb-4fd6-4197-ab9d-3d25eecaa5c6)


Tabular Column

![WhatsApp Image 2025-12-03 at 20 22 52_727275db](https://github.com/user-attachments/assets/70e6a672-3a9b-481d-9ad9-293eeb2c5a4f)


Result
The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
