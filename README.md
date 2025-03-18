## IDEAL SAMPLING
## AIM:
To Perform Contruction and Recontruction for the Ideal Sampling and Generate the Waveform for the Ideal Sampling using Numpy.
## TOOLS REQUIRED:
Python IDE with Numpy and Scipy.
## CODE:
```
#Impulse Sampling
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/f461e481-f3fd-4043-a6b2-ab66728ca50b)
![image](https://github.com/user-attachments/assets/8c0207f5-2564-4eed-a5a6-370139dc7749)
![WhatsApp Image 2025-03-18 at 11 25 39_c2303ac3](https://github.com/user-attachments/assets/9b5a54ec-fb3f-46df-933f-dfc7488a063f)

## RESULT:
The Contruction and Recontruction of the Ideal Sampling is Verified and Generated the Waveforms.




  
