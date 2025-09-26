# Fibonacci H Calculator

This is a standalone web-based calculator for generating and recovering **Fibonacci H tokens**.

## Features
- Input text (e.g., `Name|Year|ID`) → SHA-256 / HMAC-SHA256 → Fibonacci H token.
- Optional name encryption with AES-GCM + PBKDF2 (200k iterations).
- Save tokens in JSON format with encrypted names.
- Recover tokens later by loading the JSON file and entering the password.

## How to Use
1. Open `FibonacciH.html` in a modern web browser (Chrome, Firefox, Edge).
2. Enter your input text.
3. (Optional) Enter a name and password to encrypt the name in the mapping.
4. Click **Generate token** to get the SHA/HMAC and the Fibonacci H token.
5. Click **Save mapping** to download the JSON file.
6. To recover a token, open the page again, load the JSON, and provide the password.

## Verifying Integrity
We provide a SHA-256 checksum file to ensure integrity.

### Linux / macOS
```bash
shasum -a 256 FibonacciH.html
shasum -a 256 README.md
```

### Windows (PowerShell)
```powershell
Get-FileHash FibonacciH.html -Algorithm SHA256
Get-FileHash README.md -Algorithm SHA256
```

Compare the results with the values inside `CHECKSUMS.txt`.

---
Fast Science - Open Research Project  
LinkedIn: [Bogdan Marciu](https://linkedin.com/in/bogdan-marciu)
