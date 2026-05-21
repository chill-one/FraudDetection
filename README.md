# Phase 1 : Define the problem

## Problem Statement

Financial institutions process thousands of card transactions every day. Some transactions may be fraudulent due to stolen cards, unusual spending behavior, suspicious locations, repeated failed attempts, or abnormal transaction patterns. Manual review is slow, so the system needs to automatically flag suspicious transactions in near real time.

## Project Goal

- Build a real-time fraud detection system that 
    - accepts transaction data, 
    - applies fraud rules, 
    - assigns a risk score, 
    - explains why a transaction was flagged, 
    - stores the result
    - shows suspicious activity on a dashboard.


# Phase 2 : Define the users

Three main user: **Customer**, **Fraud Analyst** , **Developer**
- Cutomer : Transaction should be **protected** from fraud
- Fraud Analyst : Needs to see supicious transactions and understand why they were flagged
- Developer : Manage rules, logs, data, and system performance

**Since this is an MVP, I will mostly focus on the Fraud Analyst and Developer parts**

# Phase 3 : Define MVP scope

## MVP Features

| Feature | Description | Priority |
| ------- | ----------- | -------- |
| Submit transaction | API receives transaction data | Must-have|
| Rules-based fraud detection | System applies fraud rules | Must-have|
| Risk Score | Tansaction gets score from 0 - 100 | Must-have|
|Fraud explanation| System explains why transaction was flagged| Must-have|
|Store transaction| Save transaction and fraud result| Must-have|
|View alerts| Dashboard shows suspicious transactions | Must-have|
|View all transactions| Dashboard table for transaction history| Should-have|
|Basic metrics| Fraud rate, flagged count, total volume| Should-have|
|ML model| Predict fraud using trained model| Later|
|Graph Fraud Detection| Detect relationships between users/devices/cards| Later|
|AWS deployment| Deploy backend and database to AWS | Later|

**MVP Consist of : API + Rules Engine + Database + Basic Dashboard**



