Nice — I’ll give you a **clean, professional GitHub README.md** that matches your experiment, looks academic, and is easy for others to understand (and good for your CV too).

You can directly copy this into a file named **README.md** in your GitHub repo.

---

# 📡 Comparative Analysis of Low-Pass Filter Topologies Using Impulse Response & FFT

## 📖 Overview

This project presents a practical and analytical comparison of different low-pass filter architectures, including passive and active designs. First-order and second-order active low-pass filters were implemented and evaluated using the impulse response method combined with FFT-based frequency analysis.

The goal of this study is to observe real-world filter behavior, validate theoretical predictions, and identify the most effective low-pass filter topology for signal conditioning applications.

---

## 🔬 Filter Configurations Studied

* Passive First-Order RC Low-Pass Filter
* Active First-Order Low-Pass Filter (Op-Amp Buffered)
* Second-Order Active Low-Pass Filter (Sallen-Key Topology)
* Second-Order Active Low-Pass Filter (Multiple Feedback Topology)

All filters were designed for a nominal cut-off frequency of **3 kHz**.

---

## ⚙️ Experimental Method

* A short-duration impulse (pulse) signal was applied to each filter
* Output waveforms were captured using a digital oscilloscope
* FFT analysis was used to extract magnitude and phase responses
* Cut-off frequency, roll-off rate, stopband attenuation, and phase shift were computed using Python

---

## 📊 Tools & Technologies

* Oscilloscope with FFT capability (Keysight)
* µA741 Operational Amplifier
* Python (NumPy, Pandas, Matplotlib, SciPy)
* CSV-based waveform data acquisition

---

## 📈 Key Observations

* Active first-order filter provided the most accurate cut-off frequency
* Second-order filters achieved stronger high-frequency attenuation
* Practical results showed minor deviations due to component tolerances and op-amp limitations
* FFT-based impulse response method enabled fast and efficient frequency analysis

---

## 🚫 50 kHz Noise Consideration

A second-order active low-pass filter is most effective for rejecting high-frequency noise such as 50 kHz due to its steep attenuation beyond the cut-off frequency.

## 📁 Repository Structure

```
📂 data/
   ├── input(output).csv
   ├── passive_lowpass(output).csv
   ├── active_lowpass(output).csv
   └── second_order_outputs/

📂 scripts/
   └── Lowpass_Filter.py

📂 figures/
   └── bode_plots.png

README.md
```

---

## ▶️ How to Run the Analysis

```bash
pip install numpy pandas matplotlib scipy
python fft_analysis.py
```

---

## 🎯 Conclusion

Among the tested designs, the active first-order low-pass filter offered the best balance between accuracy and simplicity, while second-order active filters provided superior noise suppression. The impulse response and FFT-based approach proved to be an effective method for real-time filter characterization.

---

## 👤 Author

**Kavindu Gamhatha**
Electronics & Signal Processing Projects
