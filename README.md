
# Tamil Transaction Extractor & Web Dashboard

This project is a **full-stack web application** that automates the extraction of property transaction details from **Tamil PDF documents**, translates the key fields into English, stores them in a PostgreSQL database, and presents them on a modern dashboard.

It was built as a complete assignment solution demonstrating backend API design, OCR, PDF parsing, translation automation, and a responsive React (Next.js) frontend.

---

# Features

# Backend (NestJS + Node.js)
- Upload and parse Tamil property transaction PDFs  
- Text extraction using **pdf-parse** and **Tesseract.js** (OCR fallback)  
- Tamil → English translation using **LibreTranslate API**  
- Structured data storage using **Drizzle ORM** with **PostgreSQL**  
- RESTful API endpoints for:
  - `POST /api/upload` → Upload & parse PDF  
  - `GET /api/transactions` → Filter/search by buyer, seller, survey no., etc.  

# Frontend (Next.js + Tailwind CSS)
- Simple **login stub** (no authentication backend required)
- File upload interface for Tamil PDFs
- Real-time parsing progress feedback
- Table view of extracted and translated transactions
- Built-in PDF preview pane
- Clean, responsive design using Tailwind CSS

# Database (PostgreSQL + Drizzle)
- Stores both original Tamil text and translated English text
- Each record includes:
  - Buyer & Seller names (Tamil + English)
  - Survey No., Plot/House No., Document No., Date, Value
  - Raw text extracted from the PDF
  - Timestamp for ingestion

---


