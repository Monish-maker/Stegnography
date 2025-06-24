# 🕵️‍♂️🔒 Image Steganography using Python (Pillow + NumPy)

This project demonstrates how to hide secret messages inside images using a simple and effective steganography technique in Python. It uses the **Least Significant Bit (LSB)** method to encode and decode text into image pixels.

---

## ✨ Features

- Hide any text message inside an image (PNG/JPG).
- Recover the hidden message from the modified image.
- Simple implementation using **Pillow** and **NumPy**.
- Works entirely offline or in **Google Colab**.

---

## 🛠️ Tech Stack

- Python
- NumPy
- Pillow (PIL)
- Google Colab (optional)

---

## 🧠 How It Works

The algorithm modifies the **least significant bit** of each pixel's color channel (R, G, B) to embed a secret message in binary form. A special delimiter (`1111111111111110`) is used to detect where the hidden message ends.


## 🔧 How to Use

### 🖼️ 1. Upload an Image

from google.colab import files
uploaded = files.upload()
image_path = list(uploaded.keys())[0]

🔐 2. Enter Your Secret Message

secret_message = input("Enter your secret message: ")

🧬 3. Encode the Message into the Image

encode_image(image_path, secret_message, "encoded_image.png")

🔍 4. Decode the Message from the Image

decode_image("encoded_image.png")

🧪 Example Output

Enter your secret message: Hello World!
✅ Secret message hidden in encoded_image.png

Decoded message: Hello World!
📸 Notes
Supported formats: .png, .jpg, .jpeg

Do not compress the encoded image; compression may destroy hidden data.

The end delimiter (1111111111111110) marks the stop of the message.

📦 Requirements

pip install pillow numpy
Or if you're using Google Colab:
!pip install pillow numpy
