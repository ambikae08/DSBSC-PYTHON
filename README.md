# DSBSC-PYTHON
---

## Aim

To write a program to perform **Double Sideband Suppressed Carrier (DSB-SC)** modulation and demodulation using Python, and study its spectral characteristics.

---

## Apparatus Required

**Software:** Python with NumPy, SciPy, and Matplotlib libraries

**Hardware:** Personal Computer

---

## Theory

Double Sideband Suppressed Carrier (DSB-SC) modulation is a type of amplitude modulation where the carrier is suppressed, and only the two sidebands (upper and lower) carry information.
The modulated signal is given by:



---

## Algorithm

1. **Define Parameters:**

   * Sampling frequency (Fs)
   * Time duration (T)
   * Carrier frequency (Fc)
   * Message frequency (Fm)
   * Amplitude (A)

2. **Generate Signals:**

   * Message signal → sinusoidal
   * Carrier signal → high-frequency sinusoidal

3. **DSB-SC Modulation:**

   * Multiply the message and carrier signals to obtain the modulated signal

4. **DSB-SC Demodulation:**

   * Multiply the modulated signal again by the carrier
   * Apply a Butterworth low-pass filter to recover the original message signal

5. **Visualization:**

   * Plot the message signal, carrier signal, DSB-SC modulated signal, and demodulated signal

---

## Python Code

```python
import numpy as np
import matplotlib.pyplot as plt

Am=2.2
Ac=4.4
fc=2040
fm=204
fs=20400
t=np.arange(0,2/fm,1/fs)

m=Am*np.cos(2*np.pi*fm*t)
c=Ac*np.cos(2*np.pi*fc*t)
eam=(Ac+Am*np.cos(2*np.pi*fm*t))*np.cos(2*np.pi*fc*t)

plt.subplot(3,1,1)
plt.plot(t,m)
plt.show()

plt.subplot(3,1,2)
plt.plot(t,c)
plt.show()

plt.subplot(3,1,3)
plt.plot(t,eam)
plt.show()
```

---

## Output

<img width="546" height="413" alt="image" src="https://github.com/user-attachments/assets/736a06ca-6462-4211-b182-14c8cd6f0b30" />

---

## Tabulation

<img width="385" height="541" alt="image" src="https://github.com/user-attachments/assets/c74cc9ab-9631-4060-913f-3cf6ceaf3297" />



## Result

Thus, the **DSB-SC-AM modulation and demodulation** were implemented using **Python (NumPy, SciPy, and Matplotlib)**, and their spectral characteristics were successfully studied.

---
