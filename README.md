# QA Portfolio — Yevheniya Vovk

Manual QA portfolio with a small automation extension (Python).
Goal: show how I plan testing, design test cases, report bugs and verify APIs.

## Repository structure

```
qa-portfolio/
├── README.md
├── 01-test-plan/
│   └── test-plan.md            # scope, approach, risks, entry/exit criteria
├── 02-test-cases/
│   └── test-cases.md           # test cases with the design technique named
├── 03-bug-reports/
│   ├── BUG-TEMPLATE.md
│   └── BUG-001.md ...          # 8-10 real bugs with screenshots
├── 04-api-testing-postman/
│   ├── collection.json         # exported Postman collection
│   └── README.md               # what is checked and how to run it
├── 05-devtools-notes/
│   └── devtools.md             # how I investigate issues (Network / Console)
└── 06-automation-pytest/       # bonus
    └── tests/
```

## What is covered

| Skill | Where to look |
|---|---|
| Test documentation (test plan, checklist, test cases) | 01, 02 |
| Test design techniques (EP, BVA, decision table) | 02 |
| Clear bug reports | 03 |
| Postman / REST API testing | 04 |
| Chrome DevTools | 05 |
| Jira / Trello workflow | bugs are written in a Jira-style format |
| Python test automation (bonus) | 06 |

## Systems under test

- Web: https://www.saucedemo.com (public practice app)
- API: my own FastAPI project (Products Tracker) — link to repo

## Notes

All test results below were executed by me manually. Dates and browser
versions are recorded in each bug report.
