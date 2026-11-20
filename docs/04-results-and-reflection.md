# Results and reflection

## Completion record

| Module | Objective | Author-reported outcome | Evidence independently reviewed for this repository |
| --- | --- | --- | --- |
| W3-PM1 | Recover password to authorized PDF with John + Johnny | Completed | Assignment guide only; no execution proof |
| W3-PM2 | Recover password to authorized PDF with Networkwalks tools | Completed | Assignment guide only; no execution proof |

The completed status is based on my report that I finished both modules. The materials reviewed when preparing these write-ups contained the **instructions and lab files**, not my own screenshots, logs, or benchmarking data. No timing, number of guesses, exact password value or unique screenshot is claimed here.

## What I learned

### 1. File protection and password choice

A password-protected PDF is protected by an encryption scheme whose effective resistance can still be undermined by predictable passwords. A deliberately weak training password can illustrate this without suggesting that encryption itself was mathematically broken.

### 2. Hash-like tool input is not the password

The `$pdf$...` record produced by extraction tools represents information that an auditing tool uses to **validate candidates** for the document. It should not be confused with a simple hash of the plaintext password.

### 3. Local and online workflows carry different risks

Installing Johnny requires additional setup, but running John locally can give more control over the auditing environment. Online services are convenient, but uploading a protected document—or metadata extracted from it—creates a separate confidentiality decision.

### 4. Verification matters

A candidate result on a screen is only part of the audit: opening the intended training PDF using that candidate is the meaningful validation step. The source exercise explicitly included this check.

## Reproducibility notes to fill from personal records (optional)

| Detail | W3-PM1 | W3-PM2 |
| --- | --- | --- |
| Date of actual run | Not recorded | Not recorded |
| Host OS / version | Windows (version not recorded) | Windows browser (version not recorded) |
| Tool version | Not recorded | Not recorded |
| Duration | Not recorded | Not recorded |
| Password candidate count | Not recorded | Not recorded |
| Redacted screenshots | Not available | Not available |

Do **not** publish exact recovered passwords or raw protected files just to fill this table.
