# 🔥 Security Vulnerabilities in Modern Art Contest Application (Sandbox Testing)

## 📝 Overview  
This project identifies **critical security vulnerabilities** in the **Modern Art Contest** web application. Testing was conducted in a **controlled sandbox environment** to assess potential risks and provide remediation strategies.

## 🚨 Identified Vulnerabilities  
### 1️⃣ **SQL Injection in Password Reset Functionality**  
- **Endpoint:** `/forgot_password.php`  
- **Issue:** Vulnerable to SQL Injection via the email parameter, allowing attackers to retrieve **password reset tokens** and take over accounts.  
- **Impact:** Unauthorized access to user and admin accounts.  
- **Recommendation:** Implement **parameterized queries**, secure token handling, and prevent **user enumeration**.  

### 2️⃣ **Command Injection in Directory Listing Functionality** (Leads to RCE)  
- **Endpoint:** `/admin.php (Get Directory Listing Feature)`  
- **Issue:** The application **concatenates user input** directly into system commands, allowing an attacker to execute arbitrary shell commands.  
- **Impact:** **Remote Code Execution (RCE)**, granting full server control.  
- **Recommendation:** Implement **strict input validation**, use **safe execution methods**, and **restrict unauthorized access**.  

## 🧪 Testing Environment  
- **Sandbox Testing:** No real-world systems or data were impacted.  
- **Objective:** Improve web security awareness and demonstrate secure coding practices.  

## 💡 Steps to Reproduce & Screenshots  
- Detailed **steps to reproduce** each vulnerability are included in the **PDF report**.  
- **Screenshots** illustrating the exploitation process and outcomes are also provided in the PDF to visualize how the vulnerabilities can be exploited.  

## 🛡️ General Security Recommendations  
✅ Use **parameterized queries** to prevent SQL Injection.  
✅ Implement **input validation & sanitization** for all user inputs.  
✅ Secure **password reset tokens** with strong encryption.  
✅ Restrict **direct execution of user input** in system commands.  
✅ Implement **proper access controls** for admin functionalities.  

## 📂 Files Included  
- **Vulnerability Report (PDF)** – Full analysis, exploitation details, remediation, steps to reproduce, and screenshots.  
- **Code Samples** – Demonstrates both vulnerable and secure implementations.  

## 🎯 Purpose  
This project is for **educational and security research purposes only**. It aims to highlight real-world security risks and encourage **secure development practices**.  

## ⚠️ Disclaimer  
This research was performed in a **controlled, ethical testing environment**. **Do not use this information for illegal or unauthorized activities.** The findings are intended to **enhance security awareness** and **promote responsible vulnerability disclosure**.  
