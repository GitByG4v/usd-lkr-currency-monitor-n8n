# 💱 USD/LKR Currency Monitor using n8n

An automation workflow built using **n8n** that monitors the USD to LKR exchange rate and sends WhatsApp notifications whenever the exchange rate changes.

---

## Features

- Fetch live USD/LKR exchange rate
- Store previous rate using Google Sheets
- Detect increase or decrease
- Calculate exchange rate difference
- Calculate percentage change
- Send WhatsApp notifications
- Automatically update previous rate

---

## Workflow

![Workflow](screenshot.jpeg)

---

## Architecture

```text
Schedule Trigger
        │
        ▼
HTTP Request
        │
        ▼
Edit Fields
        │
        ▼
Google Sheets
(Read Previous Rate)
        │
        ▼
JavaScript
(Calculate Difference)
        │
        ▼
IF
        │
        ▼
WhatsApp Alert
        │
        ▼
Google Sheets
(Update Current Rate)
```

---

## Technologies

- n8n
- JavaScript
- Google Sheets API
- UltraMsg WhatsApp API
- Exchange Rate API

---

## WhatsApp Notification

![WhatsApp](screenshots/whatsapp-alert.png)

---

## Google Sheet

![Google Sheet](screenshots/google-sheet.png)

---

## Import Workflow

Import

```
workflow/USD-LKR-Currency-Tracker.json
```

into your n8n workspace.

---

## Configuration

Replace the following before running the workflow.

```
YOUR_API_TOKEN

YOUR_INSTANCE_ID

947XXXXXXXX
```

Connect your own

- Google Sheets account
- UltraMsg account

---

## Future Improvements

- Multiple currencies
- Historical exchange rate chart
- Daily summary report
- Threshold-based alerts
- Telegram support
- Email support

---

## Author

**Ganeshalingam Gavaskar**

Computer Science Undergraduate

Sri Lanka
