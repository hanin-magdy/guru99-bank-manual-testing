# Guru99 Bank (V4) - Manual Testing Project

A manual testing project on the Guru99 Bank V4 demo internet-banking site. I went through the full testing cycle: test plan, test scenarios, test cases, execution, bug reports, traceability matrix and a final summary report.

**Application under test:** https://demo.guru99.com/V4/

## Contents

| File | What it is |
|---|---|
| `Test_Plan.md` | Scope, approach, environment, entry/exit criteria, risks |
| `Guru99_Bank_v4_Test_Cases.xlsx` | Test scenarios, test cases with execution results, bug log, RTM, cross-version comparison |
| `Test_Summary_Report.md` | Execution numbers, defect summary, notes and conclusion |
| `screenshots/` | Evidence for the defects and key flows |

## What I tested

All 14 manager modules: Login, New/Edit/Delete Customer, New/Edit/Delete Account, Deposit, Withdrawal, Fund Transfer, Change Password, Balance Enquiry, Mini Statement, Customised Statement and Logout. For each input field I wrote positive, negative and boundary-value cases. I also ran one end-to-end flow: create customer, open account, deposit, withdraw, transfer, check statements.

I also compared V1, V2 and V3 with V4 on login, branding and available modules.

## Results

- 63 test cases designed, 46 executed (37 passed, 2 failed, 7 blocked), 17 not executed because of the time limit
- 6 defects logged (1 critical, 2 major, 1 minor, 2 trivial)
- Main finding: the transaction pages (Deposit, Withdrawal, Balance Enquiry, Mini Statement, Customised Statement) return HTTP 500 for an existing account, so the core banking flow could not be verified

All results come from running the tests on the live demo site. Details are in the Test Summary Report and the bug log sheet.

## Techniques used

Equivalence partitioning, boundary value analysis, negative testing and state transition (account balance before and after transactions).
