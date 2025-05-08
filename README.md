# 📦 PNGstagram

**Steganography for the Web — hide and reveal messages in PNG images**

---

## 🖼 What is PNGstagram?

**PNGstagram** is a minimalist web app that lets you **hide secret messages inside PNG images** using the least significant bits (LSBs) of pixel colors — right in your browser.  
No installation, no server, no trace.

---

## ✨ Features

- 🧠 Client-side steganography (no data leaves your browser)
- 📝 Encode text messages into images
- 🔍 Decode hidden messages from PNGs
- 🎨 Clean, tab-based UI
- 🔐 (Optional) Easily extendable to AES encryption or file embedding

---

## 🚀 How to Use

1. **Open `index.html`** in your browser.
2. **Encode tab**:
   - Upload a PNG image
   - Enter your secret message
   - Click “Encode & Download”
3. **Decode tab**:
   - Upload a PNG with a hidden message
   - Click “Read Hidden Message”
   - The secret is revealed!

---

## 🧪 How it Works

- Each pixel has **Red, Green, Blue, Alpha** channels (4 bytes)
- We modify the **least significant bit (LSB)** of R, G, and B to store message bits
- Message length is stored in the first 4 bytes (32 bits)
- Total: **3 bits per pixel**, invisible to the human eye

### 🧮 Data Capacity Examples

| Image Size    | Total Pixels | Usable Bits | Usable Bytes | Approx. Text Capacity |
|---------------|--------------|-------------|--------------|------------------------|
| 100 × 100     | 10,000       | 30,000      | ~3.75 KB     | ~3,750 characters      |
| 500 × 500     | 250,000      | 750,000     | ~93.75 KB    | ~90,000 characters     |
| 1000 × 1000   | 1,000,000    | 3,000,000   | ~375 KB      | ~375,000 characters    |
| 1920 × 1080   | 2,073,600    | 6,220,800   | ~777 KB      | ~750,000 characters    |

> *(Text estimates assume ~1 byte per character in UTF-8 for typical English text)*

---

## 💡 Example Use Cases

- Easter eggs in flyers or posters  
- Hidden invitations, challenge clues  
- Teaching digital privacy and steganography  

---

## 🔓 License

MIT — free to use, share, and modify.
