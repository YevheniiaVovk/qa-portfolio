# Test Cases — Sauce Demo

> The examples below are a starting point. **Run every case yourself**,
> and replace "Expected" with what the requirements/common sense say; then
> fill in "Actual" and "Status". Do not publish results you did not verify.

## Test case template

| Field | Description |
|---|---|
| ID | TC-<module>-<number> |
| Title | Short, what is being verified |
| Technique | EP / BVA / Decision table / Error guessing |
| Priority | High / Medium / Low |
| Preconditions | What must be true before the test |
| Steps | Numbered actions |
| Expected result | What should happen |
| Actual result | Filled after execution |
| Status | Pass / Fail / Blocked |

---

## Module: Login

### TC-LOGIN-001 — Login with valid credentials
- **Technique:** Equivalence partitioning (valid class)
- **Priority:** High
- **Preconditions:** Login page is open
- **Steps:**
  1. Enter username `standard_user`
  2. Enter password `secret_sauce`
  3. Click **Login**
- **Expected:** User is redirected to the products page
- **Actual:** <fill in>
- **Status:** <fill in>

### TC-LOGIN-002 — Login with valid username and wrong password
- **Technique:** Equivalence partitioning (invalid class)
- **Priority:** High
- **Steps:** username `standard_user`, password `wrong_pass`, click **Login**
- **Expected:** Error message is shown, user stays on login page
- **Actual / Status:** <fill in>

### TC-LOGIN-003 — Login with empty fields
- **Technique:** Boundary (empty value)
- **Priority:** Medium
- **Steps:** leave both fields empty, click **Login**
- **Expected:** Error that username is required
- **Actual / Status:** <fill in>

### TC-LOGIN-004 — Locked out user
- **Technique:** Error guessing
- **Priority:** Medium
- **Steps:** username `locked_out_user`, password `secret_sauce`, click **Login**
- **Expected:** Error message that the user is locked out
- **Actual / Status:** <fill in>

### TC-LOGIN-005 — Case sensitivity of username
- **Technique:** Error guessing
- **Steps:** username `Standard_User`, password `secret_sauce`
- **Expected:** <decide and justify: reject or accept>
- **Actual / Status:** <fill in>

---

## Module: Checkout — decision table

Checkout form has three required fields: First name, Last name, Postal code.

| Rule | First name | Last name | Postal code | Expected |
|---|---|---|---|---|
| R1 | filled | filled | filled | Go to overview |
| R2 | empty | filled | filled | Error: first name required |
| R3 | filled | empty | filled | Error: last name required |
| R4 | filled | filled | empty | Error: postal code required |
| R5 | empty | empty | empty | Error shown (first missing field) |

Write one test case per rule (TC-CHK-001 … TC-CHK-005) using the template.

---

## Module: Cart (boundary / state ideas)

- Add 1 item → badge shows 1
- Add all 6 items → badge shows 6
- Remove item from list page and from cart page → badge decreases
- Refresh the page with items in cart → is state kept? (record what you observe)
- Checkout with an empty cart → what happens? (record what you observe)

---

## Checklist (quick regression, 10 min)

- [ ] Login / logout
- [ ] Sort products (A–Z, Z–A, price low–high, high–low)
- [ ] Add / remove items
- [ ] Open product details and go back
- [ ] Complete checkout with valid data
- [ ] Menu → Reset App State
