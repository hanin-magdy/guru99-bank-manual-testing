# Test Summary Report - Guru99 Bank (V4)

| Field | Value |
|---|---|
| Project | Guru99 Bank V4, manual testing cycle |
| Application | https://demo.guru99.com/V4/ |
| Prepared by | Hanin Magdy, QA Engineer |
| Cycle date | November 24, 2026 |

## 1. Summary

I tested the live Guru99 Bank demo manually on 24 Nov 2026 (V4 in depth; V1, V2 and V3 compared on login and module coverage). I designed 63 test cases and executed 46: 37 passed, 2 failed and 7 were blocked. The other 17 were not executed because of the time limit. I logged six defects. The biggest finding is that every transaction page (Deposit, Withdrawal, Balance Enquiry, Mini Statement, Customised Statement) returns HTTP 500 for an existing account, so I could not verify the core banking flow.

## 2. Execution Metrics

| Metric | Count |
|---|---|
| Test cases designed | 63 |
| Test cases executed | 46 |
| Passed | 37 |
| Failed | 2 |
| Blocked / Not executed | 7 blocked, 17 not executed |
| Defects raised | 6 |

## 3. Defect Summary

| ID | Summary | Severity | Priority |
|---|---|---|---|
| BUG-01 | Typo 'Manger Id' on manager home | Trivial | Low |
| BUG-02 | New Customer accepts a future date of birth | Major | Medium |
| BUG-03 | 'Gtpl Bank' header on account-created page | Trivial | Low |
| BUG-04 | Edit Customer submit shows an empty page | Minor | Medium |
| BUG-05 | Transaction modules return HTTP 500 for existing accounts | Critical | High |
| BUG-06 | Manager pages render after logout | Major | High |

Full steps and screenshots are in the Bug Log sheet of the workbook.

## 4. Coverage

All 14 in-scope modules were covered. Traceability from requirements to test cases and defects is in the RTM sheet of `Guru99_Bank_v4_Test_Cases.xlsx`.

## 5. Exit Criteria Assessment

Exit criteria were not met. A Critical defect (BUG-05) is open, 7 cases are blocked by it and 17 cases were not executed (Edit Account, Delete Account, parts of Withdrawal, Fund Transfer, Balance Enquiry, Mini Statement, Customised Statement). My recommendation is to fix BUG-05 and BUG-06, then re-run the blocked and unexecuted cases. The 500 errors may also be a limitation of the demo site and not an application defect. This should be confirmed with the site owner.

## 6. Lessons Learned / Notes

- Test the transaction flow early next time. It is the highest-risk area and the one that failed.
- Native browser alerts block automation, so each form needs a plan for dismissing them.
- The cross-version comparison covered only login, branding and the module list. V3 Balance Enquiry also returned 500, but I did not compare V1 to V3 field by field.
- Fund Transfer with valid data returned to a blank form with no visible result, so I recorded it as Blocked, not Pass.
