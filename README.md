# ScaleBridge – Manual Testing Project

Manual QA project for **ScaleBridge**, a web-based B2B procurement platform that connects Small Businesses and Enterprise Buyers through collaborative purchasing ("Buying Circles"). Completed as part of the QA training program at **AXSOS Academy**, in a team of two testers.

The goal was to validate the deployed application against its Software Requirements Specification (SRS), find defects, and give a clear release recommendation.

## 👥 Team

| Tester | Responsibility |
|---|---|
| **Farah Talalweh** | Authentication, Dashboard & Profile, Marketplace (TC-001 – TC-042), bugs B-001 – B-006 |
| **Ibrahim Daralqorna** | Buying Circles, Orders, Reviews, Notifications, Administration, Responsive (TC-043 – TC-078), bugs B-007 – B-013 |

The application and its SRS were produced by the development team of the bootcamp (the SRS is not included in this repository).

## 🎯 Objectives

- Verify that the 20 functional requirements (FR-001 – FR-020) work as specified
- Check role-based access control (Guest, Small Business, Enterprise Buyer, Administrator)
- Evaluate responsive layout and cross-browser behavior
- Detect and document defects before release

## 🧪 Testing Performed

- Functional testing (positive and negative scenarios)
- UI testing
- Security / access-control testing (role restrictions, protected pages, session after logout)
- Responsive and cross-browser smoke testing

## 🛠️ Tools

- Microsoft Excel – test cases, bug reports, RTM, summary report
- Trello – team organisation, task assignment and daily progress tracking
- Zephyr – test management
- Jira – defect tracking
- Sauce Labs emulators and browser device simulation – cross-browser / responsive checks

## 📊 Results at a Glance

| Metric | Value |
|---|---|
| Test cases executed | **78** |
| Passed | **57** (73.1%) |
| Failed | **21** (26.9%) |
| Defects logged | **13** (9 High, 4 Medium) |
| Requirements traced (RTM) | 21 – 12 fully passing, 9 with failures |

### Results by module

| Module | Total | Pass | Fail | Pass rate |
|---|---|---|---|---|
| Administration | 12 | 7 | 5 | 58.3% |
| Authentication | 21 | 14 | 7 | 66.7% |
| Buying Circles | 9 | 8 | 1 | 88.9% |
| Dashboard & Profile | 9 | 9 | 0 | 100% |
| Marketplace | 12 | 11 | 1 | 91.7% |
| Notifications | 2 | 0 | 2 | 0% |
| Orders | 6 | 5 | 1 | 83.3% |
| Responsive | 3 | 3 | 0 | 100% |
| Reviews | 4 | 0 | 4 | 0% |

## 🐞 Key Findings

| Bug | Summary | Severity |
|---|---|---|
| B-001 | Guest role missing – guests cannot register | High |
| B-002 | Password complexity not enforced | High |
| B-003 | Password eye icon disappears on focus change | Medium |
| B-004 | Protected dashboard reachable via Back button after logout | High |
| B-005 | Password reset confirms success for unregistered email | Medium |
| B-006 | Product can be saved with price = 0 | High |
| B-007 | No review button/box on completed orders | High |
| B-008 | Notifications page missing; items not clickable | Medium |
| B-009 | No public homepage; guests land directly on login | Medium |
| B-010 | Business verification status is free text and grants no access | High |
| B-011 | Business rejection has no effect on permissions | High |
| B-012 | Status change updates the label only, not permissions | High |
| B-013 | New purchase missing from Order History | High |

## 🚦 Quality Gate Decision

**Release not recommended.** The exit criteria require no open High-severity defects, and 9 High-severity defects remain open. Recommended next steps: hand the defects to the development team, implement real verification logic on the backend, and run a full regression cycle after the fixes.

## 📂 Repository Structure

| Folder | Content |
|---|---|
| [`01-Test-Plan`](01-Test-Plan) | Scope, approach, environment, schedule, entry/exit criteria |
| [`02-Test-Cases`](02-Test-Cases) | 78 manual test cases with expected/actual results |
| [`03-RTM`](03-RTM) | Requirements Traceability Matrix (FR-001 – FR-020 + NFR) |
| [`04-Bug-Reports`](04-Bug-Reports) | 13 defect reports with steps, severity, and screenshots |
| [`05-Test-Summary-Report`](05-Test-Summary-Report) | Metrics, charts, findings and recommendations |
| [`06-Presentation`](06-Presentation) | Final QA evaluation presentation |

Each deliverable is provided as an Excel file (source) and a PDF (quick view).
