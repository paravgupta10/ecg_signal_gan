# ECG-GAN: Synthetic ECG Signal Generator

A deep-learning pipeline that generates physiologically realistic ECG heartbeats using a combination of **Autoencoders** and **Generative Adversarial Networks (GANs)**.  
This helps expand ECG datasets for healthcare AI research while preserving patient privacy.

---

## 🌟 Highlights

- ✔ Public **ECG-ID Database** used for real, subject-specific ECG recordings  
- ✔ **R-peak detection** for accurate heartbeat segmentation  
- ✔ **Uniform beat processing** via padding + smoothing  
- ✔ **Autoencoder** learns a compact latent ECG representation  
- ✔ **GAN** trained in latent space → stable & efficient generation  
- ✔ **Decoder reconstructs** full synthetic ECG waveforms  
- ✔ **RMSE analysis** for real vs synthetic quality comparison  
- ✔ **Gradio UI** for interactive synthetic ECG visualization  

---

## 📂 Dataset
- **ECG-ID Database**
- Lead I recordings
- Sampling rate: **500 Hz**
- Short sessions from multiple individuals


## 🧠 Model Workflow

Training pipeline:
1. Train Autoencoder → compress & reconstruct ECG beats  
2. Train GAN → generate new latent ECG vectors  
3. Decode GAN output → realistic synthetic ECG waveforms  


## 📊 Evaluation Metrics
We analyze the similarity between real and generated ECGs using:

- **Mean waveform RMSE**
- **Feature RMSE** (mean, variance, peak-to-peak amplitude, RMS)
These confirm waveform and statistical realism.


## 🖥️ Demo
A Gradio interface is included to:

- Select number of ECG samples
- Set random seed for reproducibility
- Visualize generated ECG beats in the browser

<img width="2924" height="1668" alt="ss" src="https://github.com/user-attachments/assets/7b800458-bc76-4ab2-bcf6-6b1302af03b7" />

