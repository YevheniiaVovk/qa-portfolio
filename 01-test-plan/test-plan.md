# Test Plan — Sauce Demo (web shop)

**Author:** Yevheniya Vovk
**Version:** 1.0
**Date:** <fill in>

## 1. Objective
Verify that the main user flows of https://www.saucedemo.com work correctly:
login, product list, cart, checkout.

## 2. Scope

**In scope**
- Login / logout
- Product list: sorting, adding to / removing from cart
- Cart
- Checkout: form validation and order completion

**Out of scope**
- Performance and load testing
- Security testing
- Mobile native apps

## 3. Test approach
- Manual functional testing based on test cases (see `02-test-cases`)
- Techniques: equivalence partitioning, boundary value analysis, decision tables
- Exploratory sessions (30–45 min each), notes saved in the bug reports
- Cross-browser smoke check: Chrome, Firefox (+ one mobile viewport in DevTools)

## 4. Test environment
| Item | Value |
|---|---|
| OS | <e.g. Windows 11> |
| Browsers | Chrome <version>, Firefox <version> |
| Tools | Chrome DevTools, Postman, Jira-style bug format |

## 5. Entry / exit criteria
- **Entry:** app is reachable, test accounts are available
- **Exit:** all test cases executed, no open Critical/Major bugs without a decision

## 6. Risks
| Risk | Mitigation |
|---|---|
| Public site may change without notice | Record date and version of every test run |
| Intentionally "problem" users (e.g. problem_user) | Document as separate findings |

## 7. Deliverables
Test cases, bug reports, short test summary.
