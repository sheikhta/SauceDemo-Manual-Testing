# Test Plan – SauceDemo (Manual Web Testing)

## 1. Overview
This test plan describes the manual functional testing of the SauceDemo website, focusing on authentication, product browsing, cart management, and checkout flows.

## 2. Objectives
- Validate core user flows of the SauceDemo application.
- Ensure correct handling of valid and invalid inputs.
- Detect UI and functional issues in critical paths.
- Provide clear test cases, bug reports, and evidence for QA portfolio purposes.

## 3. Scope

### In Scope
- Login functionality (valid, invalid, locked users).
- Product catalog display and sorting.
- Product detail page.
- Cart operations (add, remove, view cart).
- Checkout flow (information, overview, completion).

### Out of Scope
- Performance testing.
- Backend/API validation.
- Security testing.
- Full regression.
- Automation.
- Testing mobile responsiveness (focus is desktop only)

## 4. Test Types
- Manual functional testing
- Positive testing
- Negative testing
- UI validation
- Edge case testing
- Smoke testing of core flows

## 5. Test Environment & Tools
- Website: https://www.saucedemo.com/
- Browser: Google Chrome (latest)
- Tools: Google Sheets, Markdown, Screenshots
- Evidence: /evidence/ folder

## 6. Entry Criteria
- Access to SauceDemo login page
- Test data available (provided users)
- Test cases defined
- Browser installed

## 7. Exit Criteria
- All test cases executed
- Bugs documented with evidence
- Critical flow (login → add to cart → checkout) passes
- Test artifacts completed

## 8. Risks & Mitigation
- Site may reset state → repeat setup if needed
- Public test users → potential temporary login issues
- UI may vary by browser → use Chrome consistently

## 9. Deliverables
- test-plan.md
- test-cases.xlsx / test-cases.md
- bug-reports.md
- evidence/ (screenshots)
