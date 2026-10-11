# 🤖 AI-Powered Lead Scoring Automation

A fully functional, cost-effective no-code automation workflow designed to capture, analyze, and score business leads automatically using AI. Built specifically to demonstrate workflow engineering capabilities for real-world business problems.

## 🛠️ Tech Stack
- **Workflow Engine:** Make.com (formerly Integromat)
- **AI Model:** Google Gemini API (Free Tier / `gemini-flash-latest`)
- **Database/CRM:** Airtable
- **Data Trigger:** Webhook (JSON payload)

## ⚙️ How the Workflow Works
1. **Webhook Trigger:** Receives raw lead data (Name, Email, Company, Budget, Challenge) via an HTTP POST request.
2. **AI Analysis (Google Gemini):** The raw data is sent to the Gemini API with a strict prompt to act as an "expert digital agency manager". It analyzes the lead's potential and returns a structured response.
3. **JSON Parsing:** The AI's text response is parsed to extract two specific variables: `score` (Integer) and `summary` (String).
4. **CRM Logging (Airtable):** The parsed data, along with the original webhook data, is automatically mapped and saved as a new record in the Airtable "Innovative Leads" base.

## 📦 Sample JSON Payload (Webhook Input)
```json
{
  "name": "Rahim Ahmed",
  "email": "rahim@example.com",
  "company": "Dhaka Tech Solutions",
  "budget": "High",
  "challenge": "We want to automate our marketing and lead follow-up."
}
{
  "name": "Nusrat Jahan",
  "email": "nusrat@techflow.io",
  "company": "TechFlow Solutions",
  "budget": "High",
  "challenge": "Looking to integrate our existing CRM with Slack and automate our user onboarding email sequences."
}
{
  "name": "Kamal Hossain",
  "email": "kamal@dhakaproperties.com",
  "company": "Dhaka Properties",
  "budget": "Low",
  "challenge": "Want to capture Facebook lead ads and send instant SMS follow-ups to potential buyers."
}

{
  "name": "Dr. Ayesha Siddique",
  "email": "ayesha@careplus.com",
  "company": "CarePlus Clinics",
  "budget": "Medium",
  "challenge": "Need an automated appointment booking system and WhatsApp reminder workflow for patients."
}


{
  "name": "Rafiul Islam",
  "email": "rafiul@edutech.com",
  "company": "EduTech Bangladesh",
  "budget": "High",
  "challenge": "Automating student enrollment, payment tracking, and auto-generating course completion certificates."
}
