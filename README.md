# 👁️ AI Vision Table Extractor

<p align="center">
  <b>Computer Vision & AI-powered automation for extracting structured data from images</b>
</p>

---

## 📌 Overview

**AI Vision Table Extractor** is an intelligent automation workflow built with **n8n** that extracts tabular data directly from images and converts it into structured records.

The user simply sends an image containing a table through **Telegram**. The workflow uses **Google Gemini's vision capabilities** to understand the image, extract the table data, process the results using JavaScript, and automatically store the structured data in **Google Sheets**.

The project demonstrates a practical **Computer Vision + AI + Automation** pipeline for converting unstructured visual information into usable digital data.

---

## 🔄 Workflow

```text
Image / Table
      ↓
Telegram Bot
      ↓
File Download
      ↓
AI Vision Agent
      ↓
Google Gemini
      ↓
Table Data Extraction
      ↓
JavaScript Processing
      ↓
Google Sheets
      ↓
Telegram Confirmation
```

---
Screen Shot:

<img width="1837" height="590" alt="Screenshot 2026-07-30 011555" src="https://github.com/user-attachments/assets/5e5112e2-6c6b-4182-b243-ef4b82571359" />


---

## Features

 Extracts structured data from table images
 AI-powered image understanding
 Uses Google Gemini Vision
 Supports multiple rows in a single image
 Converts unstructured visual data into structured JSON
 Processes and validates extracted data with JavaScript
 Automatically stores results in Google Sheets
 Sends a confirmation message through Telegram
⚡ Fully automated end-to-end workflow

---

## 🛠️ Technologies
n8n — Workflow Automation
Google Gemini — AI Vision & Image Understanding
Telegram Bot API — Image Input & Notifications
JavaScript — Data Processing & Validation
Google Sheets — Data Storage
JSON — Structured Data Format

---

## 🧠 How It Works
1. Image Input

The user sends an image containing a table through Telegram.

The table can contain different types of structured information.
For example, the current implementation was tested with a student grade table.

2. AI Vision Analysis

The image is passed to an AI Agent connected to Google Gemini.

Gemini analyzes the visual content and identifies:

Table structure
Rows
Columns
Names or labels
Numerical values
Other readable information
3. Structured Output

The AI converts the information from the image into structured JSON.

Example:
```text
{
  "students": [
    {
      "name": "محمد أحمد",
      "english": 90,
      "arabic": 33,
      "math": 60
    },
    {
      "name": "بسنت خالد",
      "english": 44,
      "arabic": 90,
      "math": 77
    }
  ]
}
```


4. Data Processing

A JavaScript node processes the AI response and:

Parses the JSON
Removes unnecessary formatting
Validates the extracted records
Converts numerical values
Handles missing or unreadable values
Creates a consistent structure for Google Sheets


5. Data Storage

The processed records are automatically appended to Google Sheets.

6. Final Notification

After successful processing, the bot automatically sends a confirmation message through Telegram containing the Google Sheets link.

---

## 🎯 Main Concept

The core idea of the project is:
```text
Unstructured Image
        ↓
Computer Vision / AI
        ↓
Information Extraction
        ↓
Structured JSON
        ↓
Data Processing
        ↓
Digital Database
```

This eliminates the need for manually reading information from images and entering it into a spreadsheet.

---

## Use Cases

The same workflow can be adapted to extract many types of tables, such as:

📚 Student grade sheets
🧾 Invoices
📦 Inventory tables
🏢 Business reports
📋 Attendance sheets
📝 Forms
💰 Financial tables
📊 Statistical tables
🗂️ Administrative documents

The current project demonstrates the concept using a student-grade table, but the workflow can be extended to other table-based documents.

---

## 📈 Future Improvements
Support for different table structures
Automatic column detection
Improved handwritten-text recognition
Support for more document types
Automatic table validation
Duplicate detection
Export to CSV and Excel
Automatic data cleaning
Support for multiple languages
Confidence scoring for extracted values
Automatic document classification

---

## 🧩 Skills Demonstrated
Computer Vision
AI Vision
OCR / Information Extraction
Generative AI
Prompt Engineering
AI Agents
n8n Workflow Automation
JavaScript
JSON Data Processing
API Integration
Google Sheets Automation
Telegram Bot Integration
Data Transformation
End-to-End Automation

---

## 👩‍💻 Author

Rana Fayez

Data Science | Machine Learning | AI Automation

⭐ If you find this project useful, feel free to star the repository.
