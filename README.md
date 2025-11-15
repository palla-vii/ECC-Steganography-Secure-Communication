# 🔒 A Secure Elliptic Curve Based Public Key Steganography
 
This project integrates **Elliptic Curve Cryptography (ECC)** with **Image Steganography** to create a dual-layer secure communication system.  
ECC ensures **strong, lightweight public-key encryption**, while steganography hides the ciphertext inside digital images, making the message **invisible and confidential**.

---

## 📁 Repository Structure

```
ECC-Steganography-Secure-Communication
├── ECC_Steganography.ipynb       # main Colab code
├── docs
│   ├── PPT
│   ├── Report
└── README.md
```

---

## 🎥 Open Implementation (Google Colab)

Click below to run the complete project:

[Open In Colab](PASTE_YOUR_COLAB_LINK_HERE)

---

## 🚀 Features

- **Elliptic Curve Cryptography (ECC)** for secure public-key encryption
- **LSB image steganography** for hiding encrypted data inside digital images  
- **PECE / Pseudorandom Elliptic Curve Point Encoding** for random-looking ciphertext  
- Resistance to  
  - Chosen Plaintext Attack (CPA)  
  - Chosen Hidden Text Attack (CHTA)  
  - Basic steganalysis  
- High imperceptibility (PSNR, SSIM maintained)
- Lightweight and efficient design suitable for IoT and low-power devices

---

## 🧠 System Workflow

1. **Message Encryption**  
   - Convert message to bytes  
   - Encrypt using ECC public key  
   - Generate pseudorandom elliptic curve point  
2. **Steganographic Embedding**  
   - Embed ciphertext into image using LSB  
3. **Extraction & Decryption**  
   - Extract hidden ciphertext  
   - Recover plaintext using ECC private key  

A detailed explanation is available inside the **PPT PDF**.

---

## 💡 Technologies Used

- Python 3.10+  
- `cryptography` (ECC implementation)  
- `Pillow` / `OpenCV` (image processing)  
- `NumPy`, `Matplotlib`  
- Google Colab environment  
- Optional: `PyWavelets` for WaveFlow (future work)

---

## 🧪 Running the Project

### 1. Clone the repository
```bash
git clone https://github.com/palla-vii/ECC-Steganography-Secure-Communication.git
cd ECC-Steganography-Secure-Communication
```
🎯 Results

-Ciphertext successfully hidden inside images without visible distortion
-Stego images retain high PSNR & SSIM
-Receiver extracts + decrypts message correctly
-ECC provides additional security even if steganography is broken

🔭 Future Work

-Integrate WaveFlow (Wavelet + Flow-based embedding) for greater robustness
-Add DWT/DCT steganography for better resistance to compression
-Extend system to audio/video steganography
-Convert notebook into a full Python package or GUI
-Use Ristretto / Curve25519 for modern ECC encoding support

📜 License

This project is released under the MIT License.

👩‍💻 Contributors

Pallavi Sankar
Nikitha Moncy
Meghana Patil
