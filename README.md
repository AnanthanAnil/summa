# Online Banking System with Integrated Financial Tools  
**Software Design Document (SDD)**  
*Version 1.0 | Last Updated: [Date]*  

---

## Table of Contents
1. [Introduction & Purpose](#1-introduction--purpose)  
2. [Requirements](#2-requirements)  
3. [Architecture Overview](#3-architecture-overview)  
4. [Component Design](#4-component-design)  
5. [Security Considerations](#5-security-considerations)  
6. [Deployment & Operations](#6-deployment--operations)  
7. [Testing Strategy](#7-testing-strategy)  
8. [Glossary & References](#8-glossary--references)  

---

## 1. Introduction & Purpose <a name="1-introduction--purpose"></a>

### 1.1 Project Overview
Web-based platform combining:
- Core banking operations (Account Management)
- 10 financial calculators (EMI, SIP, FD, etc.)
- ML-powered loan estimation

### 1.2 Purpose
| Goal | Description |
|------|-------------|
| User Empowerment | Self-service financial planning tools |
| Operational Efficiency | Unified banking & planning interface |
| Data-Driven Insights | ML-based loan eligibility prediction |

### 1.3 Scope
**In Scope**  
✅ User authentication & session management  
✅ Account operations (balance/deposit/withdraw)  
✅ Financial calculator suite  
✅ ML loan estimator endpoint  

**Out of Scope**  
❌ Funds transfer between users  
❌ Multi-currency support  
❌ Mobile-native app  

---

## 2. Requirements <a name="2-requirements"></a>

### 2.1 Functional Requirements
**User Authentication**  
```markdown
- Endpoints:
  - `POST /api/register/` {name, email, password}
  - `POST /api/login/` {email, password}
  - `POST /api/logout/`
