________________________________________
🛡️ AI-Powered Email & Mobile Number Fraud Detection System
Advanced Fraud Analysis • Real-Time Risk Scoring • EmailRep.io Integration • Production-Ready
This repository contains an AI-powered fraud detection workflow designed to analyze email addresses and mobile phone numbers for suspicious patterns, malicious indicators, and known threat intelligence signals.
Built using n8n, this system provides accurate fraud scoring, actionable recommendations, detailed analysis, and a visually rich results dashboard.
________________________________________
🚀 Features
✅ Smart Fraud Detection Engine
•	Email risk analysis using EmailRep.io
•	Phone number fraud pattern detection (length, repetition, sequences, fake patterns)
•	Email pattern scoring (digits, vowel ratio, domain reputation, disposable domains)
•	Automatic classification into Low, Medium, and High risk tiers
🎯 Production-Grade Risk Scoring
•	Weighted scoring system
•	Capped 0–100 risk score
•	Clear risk-level actions:
o	Proceed
o	Review
o	Block / Manual Verification
🔍 Deep Email & Phone Analysis
•	Disposable domain detection
•	Malicious activity signals
•	Leaked credentials
•	Suspicious TLDs
•	Randomly generated usernames
•	Fake phone patterns (e.g., 555…, 0000000, sequences, repeated digits)
🧠 AI-Assisted Recommendations
Based on detected indicators, the system provides:
•	Identity verification steps
•	Security best practices
•	Block/review actions
•	Additional protection guidance
🌐 Beautiful Front-End Results Page
•	Dynamic animated HTML report
•	Glassmorphism UI
•	Particle effects
•	Interactive risk badge
•	Printable and export-friendly
•	“Analyze another” quick reload button
📊 Logging & Export
•	Detailed console logs
•	CSV-formatted audit entries
•	Full breakdown of sub-scores:
o	EmailRep score
o	Email pattern score
o	Phone scoring
________________________________________
📂 Project Structure
AI-Powered-Fraud-Detection/
│
├── fraud-detection-workflow.json      # n8n workflow (uploaded file)
├── README.md                          # Documentation (this file)
└── /results-page                      # HTML template rendered in the UI
________________________________________
🧩 Workflow Overview (n8n)
1️⃣ Fraud Detection Form
•	Interactive form with animated, modern UI
•	Collects:
o	Email
o	Phone number
o	Company name
o	Check purpose
2️⃣ Sanitize & Validate Input
•	Email syntax validation
•	Phone normalization to E.164
•	Invalid input returns meaningful error messages
3️⃣ EmailRep.io API Check
•	Reputation score
•	Spam / malicious indicators
•	Disposable check
•	Breach & leak data
4️⃣ Comprehensive Risk Analyzer
•	Core logic engine
•	Computes all scoring categories
•	Generates findings & recommendations
5️⃣ Output Preparation
•	Packages results for the UI
•	Formats indicators and recommendations
6️⃣ Results Page Renderer
•	Fully designed HTML report
•	Animated risk badge
•	Contact information
•	Findings
•	Recommendations
•	Timestamp & print functionality
7️⃣ Console + CSV Logger
•	Developer-friendly structured logs
•	CSV export format printed to console
________________________________________
🛠️ Requirements
•	n8n (self-hosted or cloud)
•	EmailRep.io API key (optional but recommended)
•	Node.js (bundled within n8n docker images)
•	Browser for results UI
________________________________________
⚙️ Setup Instructions
1. Import Workflow
1.	Open n8n
2.	Click Workflows → Import
3.	Upload the provided JSON file
2. Add Your API Key (Optional but recommended)
•	Add EmailRep.io API key in the HTTP Request node
•	Without this, system still works using pattern analysis only
3. Activate Workflow
•	Enable the webhook
•	Open the form URL displayed in the Trigger node
________________________________________
🖼️ Screenshots (Optional)
If you want, I can generate UI mockups or image previews for your README.
________________________________________
🧪 Example Risk Classification
Risk Level	Score Range	Action
✅ Low	0–39	Safe to proceed
⚠️ Medium	40–69	Enhanced verification required
🚨 High	70–100	Block or manual review
________________________________________
🛡️ Security Notes
•	No data is stored unless you extend logging
•	Console logs are optional
•	Recommended: integrate with SIEM or audit system
