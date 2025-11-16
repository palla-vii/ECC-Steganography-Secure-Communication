
# A Secure Elliptic Curve Based Public Key Steganography 🔒

This project integrates **Elliptic Curve Cryptography (ECC)** with **Image Steganography** to create a dual-layer secure communication system.
ECC ensures **strong, lightweight public-key encryption**, while steganography hides the ciphertext inside digital images, making the message **invisible and confidential**.

It also incorporates a **pseudorandom elliptic curve point encoding mechanism**, inspired by **Elligator-style mappings**, to ensure ciphertext appears indistinguishable from random noise.

---

## 📁 Repository Structure

```
ECC-Steganography-Secure-Communication/
├── ECC_Steganography.ipynb        # Main Colab code (includes ECC + Stego + PECE)
├── docs/
│   ├── Project_Presentation.pdf   # Final PPT (PDF)
│   ├── Report/                    # Full project report
│
└── README.md
```

---

## Open Implementation (Google Colab)

Click below to run the complete project:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ajlHyGKrhgqBRPPN20Wgqca1VnzhfgNU?usp=sharing)

---

## Features 🚀

* **Elliptic Curve Cryptography (ECC)** for secure public-key encryption
* **LSB image steganography** for embedding encrypted ciphertext into images
* **PECE — Pseudorandom Elliptic Curve Point Encoding**

  * Inspired by **Elligator-style mappings**
  * Ensures encoded curve points appear **uniform, random-looking, and non-detectable**
  * Provides stealth against statistical steganalysis
* Resistance to common attacks:

  * **Chosen Plaintext Attack (CPA)**
  * **Chosen Hidden Text Attack (CHTA)**
  * Basic steganalysis
* High imperceptibility: Maintains **PSNR & SSIM**
* Lightweight: Suitable for **IoT, mobile devices, and low-power systems**

---

## System Workflow

1. **ECC Encryption**

   * Message converted to bytes
   * Encrypted using ECC public key
   * Ciphertext point encoded using **PECE / Elligator-like mapping** to generate a “random-looking” representation
2. **Steganographic Embedding**

   * Random-looking bytes embedded into image using **LSB**
3. **Transmission**

   * Stego-image is shared
4. **Decryption**

   * Extract hidden ciphertext
   * Reverse encoding
   * Decrypt using ECC private key

Elligator-like encoding provides **plausible deniability** — ciphertext resembles random noise rather than curve points.

---

## Elligator / PECE Placeholder Explanation

This repository uses the concept of **PECE (Pseudorandom Elliptic Curve Encoding)**, which is derived from **Elligator-style encodings**:

* Maps elliptic curve points into byte strings that look *uniformly random*
* Helps avoid detectable patterns in ciphertext
* Strengthens steganography by preventing steganalysis algorithms from identifying hidden data
* Ensures ciphertext is indistinguishable from random noise to an adversary

The full Elligator2 mapping is not implemented in this version (due to complexity and curve constraints), but the notebook **contains placeholders and modular structure so Elligator can be added in the future**.

---

## Technologies Used

* Python 3.10+
* `cryptography` (ECC operations)
* `Pillow`, `OpenCV` (image steganography)
* `NumPy`, `matplotlib`
* Google Colab
* Optional (future): `PyWavelets` for WaveFlow

---

## Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/palla-vii/ECC-Steganography-Secure-Communication.git
cd ECC-Steganography-Secure-Communication
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

```
notebooks/ECC_Steganography.ipynb
```

---

## Results🎯

* Encrypted ciphertext successfully hidden without visual distortion
* High quality stego images (high PSNR/SSIM)
* Message correctly extracted and decrypted
* ECC provides additional security even if steganography is detected
* Encoded ciphertext looks random (thanks to PECE placeholder)

---

## 🔭 Future Work

* Integrate **WaveFlow (Wavelet + Flow-based embedding)** for frequency-domain robustness
* Add **full Elligator2 mapping** instead of placeholder version
* Implement **DWT / DCT domain steganography**
* Extend to **audio / video steganography**
* Build a **GUI or mobile app**
* Move to **Curve25519 / Ristretto** for modern ECC and built-in uniform encodings

---

## License

This project is released under the **MIT License**.

---

## 👩‍💻 Contributors

* **Pallavi Sankar**
* **Nikhita Moncy**
* **Meghana Patil**

---
