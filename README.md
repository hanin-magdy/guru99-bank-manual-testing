# Guru99 Bank (v4) — Manual Testing Project

End-to-end manual testing of the Guru99 Bank v4 demo internet-banking application, executed the way a QA cycle runs in a real company: planning, test design, live execution, defect reporting, traceability and closure reporting (full STLC).

**Application under test:** https://demo.guru99.com/V4/

## Contents

| File | What it is |
|---|---|
| `Test_Plan.md` | Scope, approach, environment, entry/exit criteria, risks |
| `Guru99_Bank_v4_Test_Cases.xlsx` | Test Scenarios, Test Cases with live execution results, Bug Log, RTM |
| `Test_Summary_Report.md` | Execution metrics, defect summary, lessons and sign-off |
| `screenshots/` | Evidence captured during execution (defects and key flows) |

## What was tested

All 14 manager-facing modules: Login, New/Edit/Delete Customer, New/Edit/Delete Account, Deposit, Withdrawal, Fund Transfer, Change Password, Balance Enquiry, Mini Statement, Customised Statement and Logout — with positive, negative and boundary-value cases for every input field, plus an end-to-end flow (create customer → open account → deposit → withdraw → transfer → statements).

Every result in this repository was recorded from real execution against the live demo site; no pass/fail or defect was written without observing it.


Files: Test_Plan.md, Guru99_Bank_v4_Test_Cases.xlsx (scenarios, cases and execution, bug log, RTM, cross-version, summary), Test_Summary_Report.md, Interview_Walkthrough.md, screenshots/.
