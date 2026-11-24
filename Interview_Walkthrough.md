# How I did this project (interview walkthrough)

Say it in your own words. Each step lists what to say and the evidence.

1. **Understand the app.** I read the Guru99 Bank demo, logged in as a manager and listed the modules: customers, accounts, transactions, statements. V1 has 10 menu items, V2 has 11, V3 and V4 have 15.
2. **Test Plan.** I wrote scope, out of scope, approach (functional, negative, boundary), environment, entry/exit criteria and risks (Test_Plan.md).
3. **Test Scenarios.** One scenario per module, 15 in total (Test Scenarios sheet).
4. **Test Cases.** 63 cases with ID, steps, test data, expected result. I used positive, negative, blank-field, special-character and boundary cases, for example the minimum initial deposit of 500.
5. **Execution.** I ran the cases on the live site and recorded the actual result and status for each. I never marked a case Pass without seeing the result. 37 Pass, 2 Fail, 7 Blocked, 17 Not Executed.
6. **Defects.** Six bugs with severity, priority, steps, expected and actual result and screenshots. Examples: future date of birth accepted (Major), transaction pages return HTTP 500 (Critical), manager page opens after logout (Major).
7. **Blocked cases.** I retried the 500 errors three times, then marked the cases Blocked and kept the screenshot. Be ready to say that blocked is not the same as failed.
8. **RTM.** Each requirement maps to a scenario, test case, status and defect (RTM sheet).
9. **Cross-version.** I compared V1 to V4 on login, branding and modules. Branding says "Gtpl Bank" in V1 and leaks into a V4 page (BUG-03).
10. **Closure report.** Numbers, defect summary, exit assessment and lessons (Test_Summary_Report.md).

Likely questions: severity vs priority (BUG-05 is Critical and High; BUG-01 is Trivial and Low); why some cases are not executed (time box, stated honestly); what you would do next (re-run blocked cases after a fix, then regression).
