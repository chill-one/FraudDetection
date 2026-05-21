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
- Fraud Analyst : Need to see supicious transactions and understand why they were flagged
- Developer : Manage rules, logs, data, and syste performance

**Since this is an MVP, I will mostly focus on the Fraud Analyst and Developer parts**

