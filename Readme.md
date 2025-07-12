<h1 align="center">📄 Lease Summarization Model</h1>

<p align="center">
  Extracts useful summaries from legal lease documents using OCR + NLP 🤖
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Transformers-BART-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/OCR-Tesseract-green?style=flat-square" />
</div>

---

## 🚀 Project Overview

This project is a **Lease Document Summarizer** designed to automatically extract key information from PDF lease agreements.

📌 **It reads scanned lease PDFs** (even image-based), extracts the text using **OCR**, and then uses a **powerful NLP model (BART)** to summarize the content into structured output — including:

- 🏠 Landlord and Tenant names
- 📍 Property location
- 📃 Contract duration, rental amount, and key clauses

---

## 🧠 How It Works

```
PDF (Lease) ➡️ Image ➡️ Text (via OCR) ➡️ NLP Summarizer ➡️ JSON Output
```

### 🔧 Technologies Used

- `facebook/bart-large-cnn` for summarization
- `Tesseract OCR` for scanned PDF text extraction
- `pdf2image` for converting PDF to images
- `pytesseract`, `pdfplumber` for OCR/Text
- `PHP` frontend (upload interface)
- `Python` backend for model logic

---

## 🖥 Sample Output

```json
{
  "Parties_Detail_and_Address": [
    "LEASE AGREEMENT between JOSEPH SUPOR and DOMINATE FOOD SERVICES II L.L.C.",
    "The premises are located at Harrison Avenue and Supor Boulevard Harrison New Jersey.",
    "The lease is for a period of 10 years."
  ],
  "Contract_Detail(Agreement)": "The guaranteed minimum annual rental shall be payable on the first day of each month... minimum rental will be $80,000.00 per year during years 1-20."
}
```

---

## 📁 Project Structure

```
lease-summarization-model/
├── index.php          ← Frontend upload form (PHP)
├── process.php        ← Handles file and runs Python script
├── script.py          ← Python OCR + Summarization pipeline
├── test.pdf           ← Sample lease document
├── requirements.txt   ← Python dependencies
└── README.md
```

---

## ⚙️ Setup Instructions

### 🔹 1. Clone the repo

```bash
git clone https://github.com/masfaatanveer/Lease-Summarization-Model-NLP.git
cd Lease-Summarization-Model-NLP
```

### 🔹 2. Install Python Dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install torch transformers pdf2image pytesseract pdfplumber Pillow
```

### 🔹 3. Install Tesseract OCR

#### Windows:

- Download from: https://github.com/tesseract-ocr/tesseract
- Add the installed path to your system environment variable (e.g., `C:\Program Files\Tesseract-OCR`)

#### Linux:

```bash
sudo apt install tesseract-ocr
```

### 🔹 4. Install Poppler (for pdf2image)

#### Windows:

- Download: http://blog.alivate.com.au/poppler-windows/
- Extract and add the `bin/` folder to PATH

#### Linux:

```bash
sudo apt install poppler-utils
```

---

## ▶️ Running the Project

### 💡 Run backend Python script directly:

```bash
python script.py test.pdf
```

### 💡 Run frontend locally (PHP server):

```bash
php -S localhost:8000
```

Then visit:  
📍 `http://localhost:8000`

---

## 📦 requirements.txt

```txt
transformers==4.41.1
torch>=2.0.0
pdfplumber==0.10.3
pdf2image
pytesseract
Pillow
```

---

## 👨‍💻 Developed By

**Masfa Dhillon**  
AI & Automation Developer  
[GitHub](https://github.com/masfaatanveer)

---

## 📄 License

MIT License — feel free to use, modify, and share responsibly.

---
