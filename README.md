🛠️ Well Done Construction | Worker Management System
This is a custom-built, lightweight ERP (Enterprise Resource Planning) system designed for Well Done Construction LLC. It handles everything from the first application to daily site check-ins.

🚀 System Overview
This system bridges GitHub Pages (Frontend) with Google Sheets (Database) using Google Apps Script (Engine).

Intake: New workers apply via the web form.

Onboarding: Automatic Google Drive folder creation and ID verification.

Portal: Workers access their daily checklist and upload project photos.

Admin Dashboard: Management view for the crew roster and GPS activity logs.

📂 File Structure
/admin: Crew Roster management and GPS Site Activity logs.

/application: The public-facing worker intake form.

/checklist: The daily site verification tool with GPS tracking.

/portal: The worker's home base (status, uploads, and links).

onboarding.html: The ID upload and verification page.

styles.css: The "Field-Proof" mobile-first design system.

⚡ Quick Setup (5-Minute Deployment)
Google Sheet Setup:

Create a Sheet with 6 tabs: application, CheckIns, Settings, Active Roster, ProjectLog, Archive.

Apps Script Deployment:

Go to Extensions > Apps Script in your Sheet.

Paste the Code.gs provided in this project.

Click Deploy > New Deployment (Select 'Web App', execute as 'Me', access 'Anyone').

Copy the Web App URL.

Link GitHub to the Script:

In every HTML file, find const scriptURL = '...'.

Replace the old URL with your new Web App URL.

Commit and Push to GitHub.

📋 Daily Workflow
Hire: Review applications in Google Sheets. Run the Hire Selected Applicant tool.

Assign: Use the Admin Dashboard to send job details to a worker's portal.

Verify: Check the Activity Log for GPS-stamped check-ins and Before/After photos.

Pay: Export the ProjectLog to your payroll provider every Friday.

🛠 Tech Stack
Hosting: GitHub Pages

Database: Google Sheets

Backend: Google Apps Script (JavaScript)

UI/UX: HTML5 / CSS3 (Custom "Field-Proof" Mobile Design)# welldoneconstruction.pro

# Well Done Construction Admin System

### 📊 Spreadsheet Requirements
To maintain accuracy, do not delete or reorder these columns:

#### 1. 'application' Tab
- **Col E:** Worker Email (Primary Key)
- **Col G:** Status (Auto-updates to HIRED/DOCS UPLOADED)
- **Col L:** Pay Tier (Manual entry required to enable ACTIVATE button)

#### 2. 'Settings' Tab
- **Col B:** Worker Email
- **Col E:** Job ID (Assign ID here for the Worker Portal to display it)

### 🚀 Deployment Workflow
1. Update `Code.gs` in Google Apps Script.
2. **Deploy > Manage Deployments**.
3. Edit the active deployment and select **New Version**.
4. Click **Deploy**. (This ensures all HTML files remain connected without changing URLs).
