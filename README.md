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


# Phase 4: What maybe out of Scope

## Out of Scope

| Out of Scope item | Reasons |
| ----------------- | ------- |
| Real bank data | Privacy issue but we can use Synthetically generated finanical Transaction|
| Real payment processing | Not required for this project may add it later on|
| Real card blocking | Not required for this project my add it later when deploying to AWS using Amazon SNS/Pinpoing|
| Deep learining model | Not needed for MVP but will be using it later|
| Graph neural network | Advance version later |
| real user authentication | Can add later |
| Full case mangement Workflow | Later feature |

# Phase 5: Functional Requirements (FD)

## Transaction Submission

- [ ] The system shall allow a transaction to be submitted through an API.
- [ ] The system shall require each transaction to include:
    - [ ] transaction ID
    - [ ] user ID
    - [ ] card ID
    - [ ] amount
    - [ ] merchant
    - [ ] merchant category
    - [ ] location
    - [ ] timestamp
    - [ ] device ID
    - [ ] IP address
- [ ] The system shall reject transactions with missing required fields.
- [ ] The system shall reject transactions with invalid amounts, such as negative values.
- [ ] Fraud Rule Evaluation
- [ ] The system shall evaluate each transaction using predefined fraud rules.
- [ ] The system shall increase the risk score when the transaction amount is unusually high.
- [ ] The system shall increase the risk score when multiple transactions happen within a short time window.
- [ ] The system shall increase the risk score when the transaction location is unusual for the user.
- [ ] The system shall increase the risk score when the device ID is new or suspicious.
- [ ] The system shall increase the risk score when the merchant category is high risk.


# Risk Scoring

- [ ] The system shall assign each transaction a risk score from 0 to 100.
- [ ] The system shall classify transactions as:
    - [ ] APPROVED
    - [ ] REVIEW
    - [ ] FLAGGED
- [ ] The system shall classify transactions with risk score below 40 as APPROVED.
- [ ] The system shall classify transactions with risk score from 40 to 69 as REVIEW.
- [ ] The system shall classify transactions with risk score 70 or above as FLAGGED.

## Explanation

- [ ] The system shall return the reasons why a transaction was flagged.
- [ ] The system shall display each triggered rule in the transaction result.
- [ ] The system shall allow a fraud analyst to see the risk score and explanations.

## Storage

- [ ] The system shall store every transaction in the database.
- [ ] The system shall store the fraud decision for every transaction.
- [ ] The system shall store the triggered fraud rules for audit purposes.

## Dashboard

- [ ] The system shall display total transactions processed.
- [ ] The system shall display the number of flagged transactions.
- [ ] The system shall display suspicious transactions in a table.
- [ ] The system shall allow users to view transaction details.