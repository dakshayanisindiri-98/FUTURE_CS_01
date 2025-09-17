
# Juice Shop Security Assessment – Cyber Security Internship Task 1

This repository contains the results of a web application penetration test performed on **OWASP Juice Shop** as part of my cybersecurity internship with **Future Interns**.

The purpose of this task is to demonstrate skills in **web application testing**, **vulnerability identification**, and **report generation** using **OWASP ZAP**.

---

## 📌 Project Objective
The goal of this task was to:
- Set up OWASP Juice Shop, a vulnerable web application, on a local environment.
- Configure **OWASP ZAP** as a proxy to capture and analyze network traffic.
- Perform **active vulnerability scanning** to detect security issues.
- Generate a **detailed report** and provide evidence of identified vulnerabilities.

---

## 🛠 Tools and Technologies Used

| Tool / Software        | Purpose                              |
|------------------------|--------------------------------------|
| **Windows 11**         | Operating System                     |
| **Node.js**            | Running OWASP Juice Shop             |
| **npm**                | Installing dependencies              |
| **OWASP Juice Shop**   | Target web application               |
| **OWASP ZAP**          | Intercepting traffic and scanning    |
| **Firefox Browser**    | Proxy-based testing environment      |
| **GitHub**             | Version control and submission       |

---

## ⚙️ Steps to Reproduce

### Step 1: Setup OWASP Juice Shop
1. Download Juice Shop from [GitHub Releases](https://github.com/juice-shop/juice-shop/releases).
2. Extract the files to a folder, e.g., `D:\juice-shop-19.0.0`.
3. Open Command Prompt in that folder and run:
   ```bash
   npm install
   npm start
   ```
4. Once the server starts, verify by opening:
   ```
   http://127.0.0.1:3000
   ```
<img width="3200" height="2000" alt="juice-shop-home" src="https://github.com/user-attachments/assets/52950999-bdd9-4d7e-8565-ebd3cb3bdb1f" />

📸 *Screenshot of juice-shop-HomePage *

-------------------------------------------------------------------------

### Step 2: Configure OWASP ZAP Proxy
1. Open ZAP → **Tools → Options → Local Servers/Proxies**.
2. Configure the following:
   - **Address:** `127.0.0.1`
   - **Port:** `9090`
   - **Enabled:** ✅ checked
3. Save the settings.
<img width="1472" height="1156" alt="zap-proxy-settings" src="https://github.com/user-attachments/assets/a65eac10-070a-46ba-a6a1-1c28f959c233" />

📸 *Screenshot of zap-proxy-settings *  


-------------------------------------------------------------------------

### Step 3: Configure Firefox Browser Proxy
1. In Firefox, go to:
   ```
   Settings → General → Network Settings → Settings
   ```
2. Choose **Manual Proxy Configuration** and fill:
   - **HTTP Proxy:** `127.0.0.1`
   - **Port:** `9090`
3. Clear the **"No Proxy For"** field completely.
4. Restart Firefox.

<img width="3200" height="2000" alt="Firefox-proxy-settings" src="https://github.com/user-attachments/assets/326acfd4-6376-4d60-8f4a-607733c9ee7c" />

📸 *Screenshot of firefox-proxy-settings *  

-------------------------------------------------------------------------

### Step 4: Capture Juice Shop Traffic
- Visit `http://127.0.0.1:3000` in Firefox.
- Switch to ZAP → **Sites Tab**.
- Confirm you can see:
  ```
  http://127.0.0.1:3000
  ```

<img width="1244" height="1176" alt="zap-capturing-traffic" src="https://github.com/user-attachments/assets/1383ba2e-459b-4bc7-b5ee-23b2341fc136" />

📸 *Screenshot of zap-capturing-traffic* 
 
-------------------------------------------------------------------------

### Step 5: Run Active Scan
1. In ZAP → Right-click on:
   ```
   http://127.0.0.1:3000
   ```
2. Choose:
   ```
   Attack → Active Scan
   ```
3. Leave default settings and click **Start Scan**.
4. Wait for the scan to complete.

<img width="3200" height="2000" alt="zap-scan-progress" src="https://github.com/user-attachments/assets/3be381bf-7df6-4115-9cec-61d784a850e3" />

📸 *Screenshot of zap-scan-progress *  

<img width="3200" height="2000" alt="zap-scan-result" src="https://github.com/user-attachments/assets/a75425bc-59f3-4ad5-890b-86cf527d627b" />

📸 *Screenshot of zap-scan-results *

-------------------------------------------------------------------------

### Step 6: Save Session and Export Report
1. Go to:
   ```
   File → Snapshot Session As → juice-shop-scan.session

   ```
2. Export a report:
   ```
   Report → Generate Report
   ```
   - Save as **HTML report**:
     ```
     juice-shop-vulnerability-report.html
     ```

<img width="3200" height="2000" alt="zap-html-report-preview" src="https://github.com/user-attachments/assets/5f7dd2ad-a8fa-454e-835b-df8856c663c9" />

📸 *Screenshot of zap-html-report-preview *  

-------------------------------------------------------------------------
## 📂 Project Structure

```
Task 1/
├── juice-shop-scan.session
├── juice-shop-vulnerability-report.html
├── screenshots/
│   ├── zap-proxy-settings.png
│   ├── firefox-proxy-settings.png
│   ├── juice-shop-home.png
│   ├── zap-capturing-traffic.png
│   ├── zap-scan-progress.png
│   ├── zap-scan-results.png
│   └── zap-html-report-preview.png
└── README.md
```

---

## 🔐 Key Findings

The scan identified multiple vulnerabilities with varying severity levels:

| Severity      | Count |
|---------------|-------|
| **Critical**  | Replace with count |
| **High**      | Replace with count |
| **Medium**    | Replace with count |
| **Low**       | Replace with count |
| **Informational** | Replace with count |

Example high-severity vulnerabilities detected:
- SQL Injection
- Cross-Site Scripting (XSS)
- Broken Authentication
- Sensitive Data Exposure

---

## 📜 Conclusion

This task provided hands-on experience with:
- Setting up a vulnerable web application for testing.
- Configuring ZAP for proxy-based interception and scanning.
- Identifying and analyzing real-world web application vulnerabilities.
- Documenting findings professionally in a vulnerability report.

The skills demonstrated here reflect core cybersecurity practices required for modern penetration testing and security assessment.

---

## 📧 Author
**Dakshayani Sindiri**  
Cyber Security Intern at @futureinterns 
GitHub: (https://github.com/dakshayanisindiri-98/FUTURE_CS_01)  
LinkedIn:( https://www.linkedin.com/in/dakshayani-sindiri-a55037302)





