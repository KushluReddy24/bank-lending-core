# Bank Lending System

## Overview

This repository implements a backend system for a bank lending system as per the GitLab Backend Assignment (`assignments.md` or `problems.md`). It includes RESTful API endpoints for creating loans, recording payments, viewing loan ledgers, and retrieving account overviews.

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/kushluReddt24/bank-lending-core.git
   cd bank-lending-core
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the server:
   ```bash
   node src/index.js
   ```
4. Test the API using Postman or cURL.

## Endpoints

- `POST /api/v1/loans`: Create a new loan.
- `POST /api/v1/loans/:loan_id/payments`: Record a payment.
- `GET /api/v1/loans/:loan_id/ledger`: View loan details and transaction history.
- `GET /api/v1/customers/:customer_id/overview`: View all loans for a customer.

## Database

- Uses SQLite for simplicity.
- Schema: Customers, Loans, Payments (see `src/config/db.js`).

## Notes

- Ensure a customer exists in the database before creating a loan.
- Error handling is implemented for invalid inputs and non-existent resources.
