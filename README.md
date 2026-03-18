# 🛡️ Secure Login System

![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)
![Security](https://img.shields.io/badge/security-PBKDF2--HMAC-green.svg)

A high-integrity Command-Line Interface (CLI) application designed to demonstrate industry-standard user authentication and credential protection.

---

## 🚀 Key Features

* **⚡ Smart Registration:** Real-time username availability checks.
* **Enforced Password Policies:**
    * **8+** Characters
    * **🔠** Uppercase & **🔡** Lowercase
    * **🔢** Numerical Digits
    * **✨** Special Characters (`@$!%#*?&`)
* **🚫 Brute-Force Protection:** Integrated account lockout after **3 failed attempts**.

---

## 🔒 Security Architecture

This project implements a **Zero-Plaintext** policy. We never store what the user types; we only store the mathematical proof of it.

### 1. The Hashing Pipeline
We utilize the `hashlib` and `os` modules to ensure data integrity:

* **Cryptographic Salting:** Every user receives a unique **16-byte salt** via `os.urandom()`.
* **PBKDF2-HMAC-SHA256:** We use the Password-Based Key Derivation Function 2 with **100,000 iterations**.

### 2. Implementation Specs
| Component | Implementation |
| :--- | :--- |
| **Storage** | In-memory Dictionary |
| **Hashing** | SHA-256 |
| **Iterations** | 100,000 |
| **Salt Size** | 128-bit (16 bytes) |

---

## 💻 Getting Started

### Prerequisites
* **Python 3.6+**
* No external dependencies required.

### Execution
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/secure-login-system.git](https://github.com/your-username/secure-login-system.git)
