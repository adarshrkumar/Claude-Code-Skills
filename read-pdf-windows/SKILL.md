---
name: read-pdf-windows
description: Extract text, metadata, and content from PDF files on Windows systems
when_to_use: |
  - You need to read or extract text from a PDF file
  - User mentions ".pdf" file or asks to read PDF content
  - Extracting specific pages, metadata, or tables from PDFs
  - Parsing PDF structure or content on Windows
  - Need to process multiple PDFs programmatically
---

# Reading PDFs on Windows

## Tested Pattern (Works on Windows)

Use **PyPDF2** - it's reliable and works well on Windows for basic PDF operations.

```python
from PyPDF2 import PdfReader

pdf_path = r"C:\path\to\file.pdf"
try:
    reader = PdfReader(pdf_path)
    print(f"Total pages: {len(reader.pages)}")
    
    for page_num, page in enumerate(reader.pages):
        text = page.extract_text()
        print(f"Page {page_num + 1}:\n{text}")
except Exception as e:
    print(f"Error reading PDF: {e}")
```

## Execution Pattern (Proven to Work)

**Python script + PowerShell:**

1. Write Python script to file using `Write` tool
2. Execute with `powershell python "C:\path\to\script.py"`
3. Capture output for verification

Example workflow:
```python
# save_pdf_reader.py
import os
from PyPDF2 import PdfReader

pdf_files = ["file1.pdf", "file2.pdf"]
pdf_dir = r"C:\path\to\pdfs"

for pdf_name in pdf_files:
    pdf_path = os.path.join(pdf_dir, pdf_name)
    if not os.path.exists(pdf_path):
        print(f"Skipping {pdf_name}: file not found")
        continue
    
    try:
        reader = PdfReader(pdf_path)
        print(f"{pdf_name}: {len(reader.pages)} pages")
    except Exception as e:
        print(f"Error with {pdf_name}: {e}")
```

Then execute via PowerShell and capture results.

## Windows Path Handling (Proven Pattern)

- Use raw strings: `r"C:\full\path\to\file.pdf"`
- Use forward slashes: `"C:/full/path/to/file.pdf"`
- Use `os.path.join()` for path construction
- Always check file exists before processing: `os.path.exists(path)`

## Libraries That Work

- **PyPDF2** - Tested, stable, basic PDF reading
- **pdfplumber** - Good for text extraction with tables
- Both install via: `pip install PyPDF2` or `pip install pdfplumber`

## Error Handling Pattern (Tested)

```python
import os

for file in files_to_process:
    file_path = os.path.join(directory, file)
    
    if not os.path.exists(file_path):
        print(f"Skipping {file}: file not found")
        continue
    
    try:
        # Process file
        pass
    except Exception as e:
        print(f"Error with {file}: {e}")
```
