# WP-XML (Security Audit Utility)

**WP-XML** is an auditing utility intended **only** for authorized security testing and research on WordPress instances you own or have explicit written permission to test. It helps identify whether an XML-RPC endpoint is exposed and provides configurable, lab-friendly controls for safe testing.

> **Important:** This repository does **not** provide instructions for attacking systems without authorization. Use only in controlled environments or under a signed engagement.

---

## Responsible Use & Legal Notice

- Obtain **written authorization** before testing third‑party systems.  
- Unauthorized access or password guessing is illegal and unethical. The author disclaims all liability for misuse.  
- If you plan a penetration test, include this tool in your statement of work and follow responsible disclosure rules.

---

## What this tool does (high level)

- Checks presence and basic behavior of a WordPress XML-RPC endpoint (`/xmlrpc.php`).  
- Provides concurrency, rate‑limit, timeout and proxy controls so testing can be performed safely in a lab or under an authorized engagement.  
- Emits logs suitable for inclusion in a security assessment report.  
- Designed for education, defensiveness testing, and authorized penetration testing workflows only.

*Implementation note:* written in **Go** — the language’s native concurrency primitives (goroutines, channels) make the binary efficient and portable across platforms.

---

## Prerequisites

- Go toolchain (1.18+ recommended) for building from source.  
- Git (to clone repo).  
- A controlled test environment (local WordPress instance or isolated VM) when performing any kind of authentication testing.  
- Written permission from the owner when testing systems you do not personally own.

---

## Installation / Build (developer / lab)

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd <repo-directory>
