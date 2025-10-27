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

Am=2.1
Ac=4.2
fc=2030
fm=203
fs=20300
beta=3.6
t=np.arange(0, 2/fm, 1/fs)
m=Am* np.cos(2*np.pi*fm*t)

c=Ac* np.cos(2*3.14*fc*t)

efm=Ac*np.cos((2*np.pi*fc*t)+beta*np.sin(2*np.pi*fm*t))

plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.show()

plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.show()

plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.show()
```

Output Waveform

<img width="552" height="152" alt="image" src="https://github.com/user-attachments/assets/7d597749-a277-4232-aea4-d1225199b2c3" />
<img width="565" height="152" alt="image" src="https://github.com/user-attachments/assets/2dd8c291-af3f-4e5a-a833-d11544bd9555" />
<img width="565" height="152" alt="image" src="https://github.com/user-attachments/assets/126a9b3e-bf73-42ed-aeb8-2e17300f088f" />

Tabular Column

![WhatsApp Image 2025-10-27 at 17 03 56_234a25e9](https://github.com/user-attachments/assets/885478a3-3e26-498f-a9b5-9bf466261b95)

Calculation

![WhatsApp Image 2025-10-27 at 17 03 58_debb246e](https://github.com/user-attachments/assets/83971005-5a9b-4fc6-8fdb-1aa9a6357fce)

Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
