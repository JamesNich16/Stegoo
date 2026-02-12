Steganography – Easy-to-Use Image Hiding Tool (Stego)

Stego is a smart and secure tool that lets you hide secret files inside images without anyone noticing.
It combines strong cryptography with AI-assisted steganography to keep your data private, protected, and hard to detect.

Key Features

✔ Strong Protection
Your hidden file is encrypted using AES-256 + RSA, the same standards used in banking and government systems.
Only someone with the correct private key can extract the data.

✔ Compression
Files are compressed before hiding, reducing size and lowering detection risk.

✔ AI-Assisted Adaptive LSB (NEW)
Stego uses an AI-based texture analysis to intelligently choose safe pixels (edges and textured regions) for hiding data.
This makes changes less noticeable and improves resistance to steganalysis.

✔ Smart Hiding Technique (LSB Steganography)
Hidden data is embedded using Least Significant Bit (LSB) modification, causing no visible change to the image.

✔ Preserves Filenames
Extracted files automatically retain their original filenames.

✔ Cross-Platform
Works on Windows, macOS, and Linux using Python.

AI-Assisted Adaptive LSB (How It Works)

Instead of hiding data in random pixels only, Stego now:

Analyzes the image using AI-based texture/variance analysis

Identifies high-complexity regions (edges, noisy areas)

Embeds data only in these safer pixels

Uses the same AI logic during extraction for perfect recovery

Why this matters

Changes are harder for the human eye to notice

Statistical steganalysis becomes more difficult

Security is improved without changing the encryption logic

This approach uses classical AI / machine-learning principles (feature extraction + decision logic), not heavy deep learning — making it fast, reliable, and exam-friendly.

Installation

Clone the repository and install dependencies:

pip install -r requirements.txt

Generate Encryption Keys

Create a public/private key pair:

python generate_keys.py


You’ll be asked to enter a strong passphrase.

This generates:

myprivatekey.pem → Keep this secret

mypublickey.pem → Safe to share

How to Use

1️⃣ Hide a File Inside an Image
python secret_pixel.py hide host.png secret.txt mypublickey.pem output.png

Parameters:

host.png – Cover image (PNG/BMP/TIFF recommended)

secret.txt – File to hide

mypublickey.pem – Public key for encryption

output.png – Image containing the hidden file

2️⃣ Extract a Hidden File
python secret_pixel.py extract output.png myprivatekey.pem [extracted.txt]


Parameters:

output.png – Image with hidden data

myprivatekey.pem – Private key for decryption

extracted.txt (optional) – Output filename
(If omitted, the original filename is restored)

🔐 Why Stego Is Secure & Hard to Detect

Military-Grade Encryption
AES-256 + RSA hybrid encryption protects data confidentiality.

AI-Driven Pixel Selection
AI selects visually complex regions, reducing detection risk.

Randomized & Adaptive Embedding
No predictable hiding pattern.

Lossless Image Formats
Best used with PNG, BMP, TIFF, or TGA to preserve hidden data.

Steganalysis Resistant
Difficult for tools like zsteg to detect hidden content.

Want to Help Improve Stego?

You’re welcome to:

Report bugs or suggest new features

Improve performance or security

Enhance documentation

Submit Pull Requests

📝 Final Thoughts

Stego combines cryptography + AI-assisted steganography to provide a powerful yet simple way to hide files inside images.
Whether for privacy, security research, or learning, it keeps your data hidden, encrypted, and safe.

🚀 Get started now and hide your secrets like a pro!
