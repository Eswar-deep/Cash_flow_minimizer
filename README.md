# Cash Flow Minimizer System

## Overview
The **Cash Flow Minimizer System** is a tool designed to minimize the number of financial transactions between multiple banks. It ensures that all payments are completed efficiently, even when banks use different payment modes, with the help of a central `World Bank` that supports all payment modes.

---

## Features
- Calculates the net amount owed or to be received by each bank.
- Handles payment transactions using different modes (`QuickPay`, `SafePay`, `FlexiTransfer`).
- Uses a central `World Bank` as an intermediary for banks without common payment modes.
- Outputs the minimized number of transactions and details of each transaction.

---

## Input
1. **Number of Banks**: Total number of participating banks.
2. **Bank Details**: For each bank:
    - Bank name (no spaces).
    - Number of payment modes.
    - List of payment modes.
3. **Number of Transactions**: Total number of transactions.
4. **Transaction Details**: For each transaction:
    - Debtor bank.
    - Creditor bank.
    - Amount to be transferred.

---

## Output
- Optimized list of transactions that minimize the number of transfers.
- Details include:
  - Amount.
  - Debtor bank.
  - Creditor bank.
  - Payment mode.

---

## How to Run
### Prerequisites
- A C++ compiler (e.g., `g++`).

### Steps
1. Clone the repository or download the source code.
2. Compile the code using the following command:
   ```bash
   g++ cash_flow_minimizer.cpp -o cash_flow_minimizer
   ```
3. Run the executable:
   ```bash
   ./cash_flow_minimizer
   ```
4. Follow the prompts to enter the required inputs.

---

## Example Usage
### Input
```
Number of Banks: 3
Bank Details:
  - Bank 1: Alpha, 2 modes (QuickPay, SafePay)
  - Bank 2: Beta, 1 mode (FlexiTransfer)
  - Bank 3: WorldBank, 3 modes (QuickPay, SafePay, FlexiTransfer)

Number of Transactions: 2
Transactions:
  - Alpha pays Beta Rs 100
  - Beta pays Alpha Rs 50
```

### Output
```
The transactions for minimum cash flow are as follows:
Alpha pays Rs50 to Beta via QuickPay
```

---

## Code Structure
- **`bank` class**: Stores information about each bank.
- **`getMinIndex()`**: Finds the bank with the minimum net amount.
- **`getMaxIndex()`**: Finds the bank with the maximum net amount.
- **`printAns()`**: Outputs the minimized transactions.
- **`minimizeCashFlow()`**: Core logic for minimizing cash flow using the Greedy algorithm.

---

## Contact
For any queries or feedback, please contact the developer.
