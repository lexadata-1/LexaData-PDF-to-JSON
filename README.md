# LexaData: The Invisible API for PDF to JSON
### No SDKs. No API Keys. Just Email.

LexaData converts complex PDFs (invoices, legal documents, reports) into structured JSON using a simple email interface. Perfect for legacy systems, No-Code workflows (Zapier/Make), and quick data engineering tasks.

## 🚀 How to use

1. **Compose an email** to: `recepcao.lexadata@gmail.com`
2. **Attach your PDF** file (Text or Scanned/OCR).
3. **Send.**
4. Within seconds, you will receive a reply with the **JSON file attached**.

## ⚡ Integration Example (Python)

You don't need a library. You just need SMTP.

```python
import smtplib
from email.message import EmailMessage

msg = EmailMessage()
msg['Subject'] = 'Extract Data'
msg['From'] = 'me@company.com'
msg['To'] = 'recepcao.lexadata@gmail.com'

# Attach your PDF
with open('invoice_1023.pdf', 'rb') as f:
    file_data = f.read()
    msg.add_attachment(file_data, maintype='application', subtype='pdf', filename='invoice.pdf')

# Send
with smtplib.SMTP('smtp.gmail.com', 587) as s:
    s.login('me@company.com', 'password')
    s.send_message(msg)

print("File sent! Check your inbox for the JSON response.")


💰 Pricing
Currently in Public Beta (Free).

🔒 Privacy & Security
Files are processed in memory and discarded after extraction.

We do not use your data to train public models.
