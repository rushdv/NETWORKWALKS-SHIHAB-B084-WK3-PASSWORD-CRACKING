# Password Cracking Lab — Hash Extraction & Dictionary Attacks
**Week 03 | Networkwalks Cybersecurity Internship (Batch: B084)**

---

## 📌 Project Overview
This repository contains the lab documentation, hash extraction workflows, recovered passwords, captured flags, and visual evidence for **Week 03** practical tasks under the Networkwalks Cybersecurity Program.

- **Security Analyst:** Md. Shihab Shahriar Rashu
- **Program / Batch:** B084-Networkwalks
- **Modules Covered:**
  - `W3-PM1`: Password Cracking with John the Ripper (JTR CLI / Johnny)
  - `W3-PM2`: Password Cracking with Networkwalks Tools (Hash Calculator & Dictionary Password Cracker)

---

## 🛠️ Tools & Techniques Used
- **Hash Extraction:** Networkwalks Hash Calculator (`$pdf$` hash extraction) & `pdf2john`
- **Password Auditing / Cracking:** Networkwalks Dictionary Password Cracker (with JTR default wordlist) & John the Ripper (JTR)
- **Attack Methodology:** Offline Dictionary-Based Hash Matching

---

## 🚩 Recovered Passwords & Captured Flags Summary

| Target File | Encryption / Hash Format | Recovered Password | Captured Flag |
| :--- | :--- | :--- | :--- |
| **Locked PDF 1** | `$pdf$4*4*128*...` | `good-luck` | `nw{cybersecurity_flag_captured_2608}` |
| **Locked PDF 2** | `$pdf$4*4*128*...` | `password1` | `nw{networkwalks_persistence_jtr_270521}` |
| **Locked PDF 3** | `$pdf$4*4*128*...` | `1qaz2wsx` | `nw{networkwalks_flag_260821_1}` |

---

## 🔍 Key Takeaways
1. **Predictable Passwords Fail Rapidly:** Common words and keyboard patterns (`password1`, `1qaz2wsx`, `good-luck`) are recovered within seconds against standard wordlists (`3,556` entries).
2. **Offline Hash Vulnerability:** Once an encrypted file's cryptographic hash (`$pdf$`) is extracted, attackers can perform offline dictionary or brute-force attacks without triggering account lockout mechanisms.
3. **Mitigation:** Sensitive documents should be protected using high-entropy passphrases (14+ mixed characters) and modern AES-256 encryption standards.

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
