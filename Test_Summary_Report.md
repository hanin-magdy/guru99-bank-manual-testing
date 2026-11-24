# Test Summary Report — Guru99 Bank (v4)

| Field | Value |
|---|---|
| Project | Guru99 Bank v4 — manual testing cycle |
| Application | https://demo.guru99.com/V4/ |
| Prepared by | Hanin Magdy — QA Engineer |
| Cycle date | November 24, 2026 |

## 1. Summary

Testing was done manually on the live Guru99 Bank demo (V4 in depth; V1, V2 and V3 compared on login and module coverage) on 24 Nov 2026. 63 test cases were designed; 46 were executed (37 Pass, 2 Fail, 7 Blocked) and 17 were not executed because of the time box. Six defects were logged. The biggest finding is that every transaction page (Deposit, Withdrawal, Balance Enquiry, Mini Statement, Customised Statement) returns HTTP 500 for an existing account, so the core banking flow could not be verified.

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

Exit criteria were not met. A Critical defect (BUG-05) is open, 7 cases are blocked by it and 17 cases were not executed (Edit Account, Delete Account, parts of Withdrawal, Fund Transfer, Balance Enquiry, Mini Statement, Customised Statement). Recommendation: fix BUG-05 and BUG-06, then re-run the blocked and unexecuted cases. The 500 errors may also be a demo-site limitation, not an application defect, and this should be confirmed with the site owner.

## 6. Lessons Learned / Notes

- Start with the transaction flow early, since it is the highest-risk area and the one that failed.
- Native browser alerts block automation, so each form needs a plan for dismissing them.
- Cross-version comparison was limited to login, branding and module list. V3 Balance Enquiry also returned 500; field-level comparison of V1 to V3 was not done.
- Fund Transfer with valid data returned to a blank form with no visible result, so it was recorded as Blocked, not Pass.
