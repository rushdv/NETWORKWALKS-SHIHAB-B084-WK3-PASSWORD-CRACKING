# Password Cracking Lab — Hash Extraction & Dictionary Attacks
**Week 03 | Networkwalks Cybersecurity Internship (Batch: B084)**

---

## 📌 Project Overview
This repository contains the lab documentation, hash extraction workflows, recovered passwords, captured flags, and visual evidence for **Week 03** practical tasks under the Networkwalks Cybersecurity Program.

- **Security Analyst:** Md. Shihab Shahriar Rashu
- **Program / Batch:** B084-Networkwalks
- **Modules Covered:**
  - `W3-PM1`: Password Cracking with John the Ripper (JTR CLI / Johnny)[cite: 52]
  - `W3-PM2`: Password Cracking with Networkwalks Tools (Hash Calculator & Dictionary Password Cracker)[cite: 44]

---

## 🛠️ Tools & Techniques Used
- **Hash Extraction:** Networkwalks Hash Calculator (`$pdf$` hash extraction) & `pdf2john`[cite: 44, 46]
- **Password Auditing / Cracking:** Networkwalks Dictionary Password Cracker (with JTR default wordlist) & John the Ripper (JTR)[cite: 44, 52, 67, 69, 71]
- **Attack Methodology:** Offline Dictionary-Based Hash Matching[cite: 47]

---

## 🚩 Recovered Passwords & Captured Flags Summary

| Target File | Encryption / Hash Format | Recovered Password | Captured Flag |
| :--- | :--- | :--- | :--- |
| **Locked PDF 1** | `$pdf$4*4*128*...`[cite: 71] | `good-luck`[cite: 71] | `nw{cybersecurity_flag_captured_2608}`[cite: 70] |
| **Locked PDF 2** | `$pdf$4*4*128*...`[cite: 69] | `password1`[cite: 69] | `nw{networkwalks_persistence_jtr_270521}`[cite: 68] |
| **Locked PDF 3** | `$pdf$4*4*128*...`[cite: 67] | `1qaz2wsx`[cite: 67] | `nw{networkwalks_flag_260821_1}`[cite: 66] |

---

## 📸 Visual Evidences & Lab Outputs

### 1. Locked PDF 1 (`good-luck`)[cite: 71]
**Password Cracked Output:**
![PDF 1 Cracked](screenshots/pdf1-cracked.jpg)

**Captured Flag Verification:**
![PDF 1 Flag](screenshots/pdf1-flag.jpg)

---

### 2. Locked PDF 2 (`password1`)[cite: 69]
**Password Cracked Output:**
![PDF 2 Cracked](screenshots/pdf2-cracked.jpg)

**Captured Flag Verification:**
![PDF 2 Flag](screenshots/pdf2-flag.jpg)

---

### 3. Locked PDF 3 (`1qaz2wsx`)[cite: 67]
**Password Cracked Output:**
![PDF 3 Cracked](screenshots/pdf3-cracked.jpg)

**Captured Flag Verification:**
![PDF 3 Flag](screenshots/pdf3-flag.png)

---

## 🔍 Key Takeaways
1. **Predictable Passwords Fail Rapidly:** Common words and keyboard patterns (`password1`, `1qaz2wsx`, `good-luck`) are recovered within seconds against standard wordlists (`3,556` entries)[cite: 44, 67, 69, 71].
2. **Offline Hash Vulnerability:** Once an encrypted file's cryptographic hash (`$pdf$`) is extracted, attackers can perform offline dictionary or brute-force attacks without triggering account lockout mechanisms[cite: 44].
3. **Mitigation:** Sensitive documents should be protected using high-entropy passphrases (14+ mixed characters) and modern AES-256 encryption standards[cite: 50].

---

## 📁 Repository Structure
```text
├── README.md
└── screenshots/
    ├── pdf1-cracked.jpg
    ├── pdf1-flag.jpg
    ├── pdf2-cracked.jpg
    ├── pdf2-flag.jpg
    ├── pdf3-cracked.jpg
    └── pdf3-flag.png
