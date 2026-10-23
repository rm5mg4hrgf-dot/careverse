# CAREVERSE

**Test the workflow. Expose the failure. Improve the system.**

CAREVERSE is a static, browser-based hospital workflow simulation prototype for DSH Hacks V2 (AI × Healthcare). It uses fictional records and deterministic rule-based checks to demonstrate how workflow safeguards can expose synthetic information inconsistencies.

## GitHub Pages deployment

This is a plain static website: no Node.js build, package installation, server, API key, or backend is required.

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Commit or push to `main`; the included workflow validates the HTML/JavaScript and deploys the static site automatically.
4. Open the **Actions** tab and wait for **CAREVERSE — Validate and Deploy** to finish successfully. The entry point is the root `index.html`.

Expected project URL: https://rm5mg4hrgf-dot.github.io/careverse/

## Current prototype features

- Command Center with run metrics, latest flagged evidence, recent runs, and quick start.
- Hospital Simulator with three synthetic departments, patient-flow events, scenario selection, and deterministic seeds.
- Ten searchable synthetic scenarios with severity labels.
- Failure Replay timeline, record-field comparison, seeded replay, and rule-based explanation fallback.
- Six configurable safeguards that change which matching inconsistencies are detected.
- Experiment Lab comparing safeguards-off and current-configuration runs using identical scenario and seed inputs.
- Evidence & Audit with run metadata and JSON/CSV exports.
- Responsive navigation and layouts, accessible form labels, focus styles, and reduced-motion support.

## Important limitations

- This is a front-end research demonstration, not a medical device or clinical decision-support system.
- All patient records and workflow outcomes are synthetic. Do not enter real patient information.
- Explanations are deterministic and rule-based; no external AI model is connected.
- Runs are held in the current page session. The prototype does not provide durable database storage, user accounts, multi-user collaboration, or a backend.
- The experiment sample size is one paired run per selected scenario; its results are demonstrations, not clinical performance estimates.

## Verification

The included GitHub Actions workflow checks the HTML entry point, detects duplicate IDs, checks inline JavaScript syntax with Node.js, verifies key app markers, and deploys the root directory to GitHub Pages. This is static validation, not a full automated browser or clinical validation suite. After deployment, manually test the interactive flows in a browser.
