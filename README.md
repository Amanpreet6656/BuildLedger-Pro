# BuildLedger Pro: Construction Payroll Management System

This repository contains the source code for BuildLedger Pro, a bilingual single-page application engineered to manage construction workforce attendance and precise payroll computation.

## Architectural Overview

The application operates on a zero-backend, purely client-side architecture. It utilizes Vanilla JavaScript for complex state management, data validation, and DOM manipulation, and is styled with Tailwind CSS for hardware-accelerated rendering. 

Data persistence is handled entirely via the browser's Web Storage API (LocalStorage). This design choice ensures robust offline functionality, allowing continuous data entry and retrieval in remote construction site environments where network connectivity is limited or unavailable.

## Core Functional Modules

* **Algorithmic Payroll Ledger:** Dynamically computes real-time wage balances for individual workers. The engine calculates gross pay by aggregating the base daily rate and total accumulated working days, subsequently subtracting any logged advance cash disbursements to determine the final balance due.
* **State-Driven Attendance Matrix:** Features a localized daily attendance system that evaluates present (1.0), half-day (0.5), and absent (0.0) states. Each logged state automatically recalculates the worker's total accrued days and triggers an immediate update to their financial ledger.
* **Dynamic Localization (i18n):** Implements an integrated state controller to seamlessly toggle the Document Object Model (DOM) text and interface placeholders between English and Hindi without requiring page reloads or external API calls.
* **Client-Side Data Serialization:** Incorporates a custom parsing function that converts current LocalStorage state arrays into a formatted CSV string, generating a downloadable file via a localized Blob URL for external administrative review and record-keeping.
* **System-Aware Theming:** Includes a functional dark/light mode toggle that leverages Tailwind's class-based dark mode configuration to reduce ocular strain in low-light environments.

## Technical Stack

* **Frontend Infrastructure:** HTML5, CSS3, Tailwind CSS (via CDN)
* **Application Logic:** Vanilla JavaScript (ES6+)
* **Data Persistence:** Web Storage API (LocalStorage)
* **Typography & Iconography:** Google Fonts (Inter, Poppins), FontAwesome

## Local Execution

To run the application locally, no build steps, package managers, or local server environments are required.

1. Clone this repository to your local directory.
2. Open the `index.html` file directly in any modern web browser.
