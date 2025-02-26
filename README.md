# stentography-project
# 🖼️ Image Steganography - Hide & Extract Secret Messages

## 📌 Overview
This project implements **Image Steganography** using the **Least Significant Bit (LSB) encoding technique** to hide secret messages inside images without noticeable visual changes. The encoded image can later be used to extract the hidden message.

## 🚀 Features
- **Secure Message Hiding**: Encodes text messages into image files discreetly.
- **Password Protection**: Ensures that only authorized users can decrypt messages.
- **LSB Encoding**: Uses the Least Significant Bit technique for data embedding.
- **Multiple Format Support**: Works with PNG, JPEG, and BMP images.
- **Lossless Encoding**: The image remains visually unchanged after encoding.
- **Command-Line Interface**: Easy-to-use CLI for encoding and decoding.

## 🛠️ Technologies Used
- **Python**
- **Pillow (PIL)** - Image processing
- **OpenCV** - Computer vision tasks
- **NumPy** - Efficient array operations
- **argparse** - CLI argument handling

## 📥 Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/TusharSinh96/stentography-project.git
   cd stentography-project
   ```
2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## 📝 Usage
### **1️⃣ Encoding a Message into an Image**
```sh
python steganography.py --encode input.png --data "Your Secret Message" --output output.png
```
- `input.png` → Original image
- `"Your Secret Message"` → Message to be hidden
- `output.png` → Encoded image with the hidden message

### **2️⃣ Decoding the Hidden Message**
```sh
python steganography.py --decode output.png
```
- Extracts and prints the hidden message from `output.png`

## 🖼️ Example
### **Original Image**
![Original Image](assets/original.png)

### **Encoded Image (Visually Identical but Contains a Message)**
![Encoded Image](assets/encoded.png)

### **Extracted Secret Message**
```
Extracted Secret Data: "Hello, this is a hidden message!"
```

## 🔐 How It Works
1. Converts text into binary format.
2. Modifies the **least significant bit (LSB)** of pixel values to embed the message.
3. Appends an **end delimiter** (`1111111111111110`) to indicate the end of the message.
4. Extracts the hidden message by reading the LSB values from the encoded image.

## 📌 Future Scope
- **Enhanced Security**: Implement stronger encryption alongside steganography.
- **Larger Capacity**: Optimize encoding to store more data.
- **Cross-Platform GUI**: Develop a user-friendly interface.
- **Multi-Media Support**: Extend the technique to **audio and video steganography**.

## 🤝 Contributing
Contributions are welcome! Feel free to fork this repo and submit a pull request.

## 📜 License
This project is licensed under the **MIT License**.

## 🔗 GitHub Repository
[🔗 View on GitHub][https://github.com/TusharSinh96/stentography-project.git]

---
🚀 *Developed with ❤️ by [Tushar Dayatar]*
