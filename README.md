✅ Features
🔍 Syntax Validation — Ensures the email follows proper formatting.
🌐 MX Record Lookup — Checks if the email domain is valid and has mail servers configured.
📡 SMTP Verification — Connects to the mail server to check if the specific email address exists (if the server allows).
📁 Batch Processing — Validates multiple emails from text files in bulk.
📤 Export Valid Emails — Saves verified emails into an export directory.
💡 Console Feedback — Real-time logging for each verification step.

📂 Folder Structure 
📁 your_project_folder/
│
├── 📁 pasta_emails/       # Input folder with .txt files containing email lists
│   ├── list_A.txt         # Example: list of emails to check
│   └── list_B.txt
│
├── 📁 export/             # Output folder for valid emails (auto-created if missing)
│   └── valid_list_A.txt    # Valid emails will be saved here
│
├── 📄 run.py              # Main Python script
└── 📄 README.md           # Documentation file (this file)
⚙️ How It Works
Place your email lists (one email per line) in the pasta_emails folder.
Run the script to validate the emails.
Valid emails are saved in the export folder.
🏁 How to Run the Script
Clone the repository:
git clone https://github.com/yourusername/email-verifier-script.git
cd email-verifier-script
Install the required dependencies: 
pip install dnspython
Run the script: 
python run.py

💾 Input Example (pasta_emails/list_A.txt)
valid.email@example.com
invalid.email@nonexistentdomain.xyz
test.email@gmail.com
wrongformat@com

📊 Console Output Example 
📂 Processing file: list_A.txt

➡️ Checking email: valid.email@example.com
🔎 Domain 'example.com' has valid MX records.
✅ Email exists and is valid.

➡️ Checking email: invalid.email@nonexistentdomain.xyz
❌ Domain 'nonexistentdomain.xyz' has no MX records.

➡️ Checking email: test.email@gmail.com
⚠️ SMTP verification not allowed by the server.

➡️ Checking email: wrongformat@com
❌ Invalid email syntax.

✅ 1 valid email exported to: export/valid_list_A.txt

🚀 Verification completed. Check the 'export' folder for results.


⚡ Limitations
Some mail servers (like Gmail, Outlook, Yahoo) may block SMTP verification attempts or always return a "valid" response for privacy reasons.
High-volume verifications can lead to IP blacklisting by some mail providers.
This script does not send emails; it only checks if an email can receive emails.
💡 Tips for Better Accuracy
Consider using verified email validation services like Hunter.io, ZeroBounce, or NeverBounce for large-scale verifications.
When verifying sensitive domains, use dedicated or rotating IPs to avoid blocking.
🤝 Contributing
Feel free to submit pull requests or open issues if you have suggestions or improvements.
 





