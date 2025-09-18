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

Am=2.3
Ac=4.6
fc=2170
fm=217
fs= 21700
beta=2.4
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
plt.plot(t,efm)
plt.show()
```

Output Waveform
<img width="1228" height="677" alt="image" src="https://github.com/user-attachments/assets/b13e290c-7e47-414f-b324-8b8595723bd9" />


Tabular Column


![Uploading image.png…]()



Calculation




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
