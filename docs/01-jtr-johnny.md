# W3-PM1 — Password auditing with John the Ripper and Johnny GUI

**Status:** Completed, as reported by the repository author.  
**Assigned objective:** Recover access to the provided `My Locked PDF1.pdf` training file with John the Ripper and Johnny GUI on Windows.

## 1. Why I did this

This lab demonstrated how password auditing can reveal weak protection on a PDF. I wanted to understand both the input preparation process and the role of a graphical interface when operating a command-line security tool.

## 2. Tools and setup

- Windows computer
- John the Ripper (the password-auditing engine)
- Johnny (graphical front end for John)
- Authorized password-protected training PDF
- PDF-to-John-compatible extraction method described in the assignment

The instructor's workflow used an online PDF hash extractor. For *confidential files*, a local, trusted extraction process is a safer alternative; no confidential file should be uploaded for convenience.

## 3. Lab process

1. **Prepared the environment.** Installed/obtained John the Ripper and Johnny from their project sources.
2. **Connected the tools.** Configured Johnny's settings to locate the `john.exe` executable in the John installation's `run` directory.
3. **Prepared an audit input.** Used the PDF extractor described by the lab to obtain a John-compatible `$pdf$...` string and placed it into a local text file (the task names it `hash1.txt`).
4. **Loaded the audit input.** Used Johnny's **Open password file** action to import the prepared text file.
5. **Ran the password test.** Started an authorized audit from Johnny and observed the tool attempt candidate passwords against the extracted file data.
6. **Validated the lab objective.** The final check in the exercise was to open the assigned PDF using the recovered password.

> The steps above reflect the prescribed task workflow and author-reported completion. They are not accompanied by independent logs, timings or screenshots from the author's run.

## 4. Where John fits

Johnny provides the interface; **John the Ripper is the engine** that tests password candidates. Extracted PDF audit data is not a reusable login token and is not the plaintext password. Its exact format depends on the encrypted PDF and the extraction tool.

The exercise used the GUI. For reference only, John also supports a command-line interface; do not interpret the following as a transcript of my own run:

```powershell
# Illustrative only; requires an authorized lab hash file and installed John
.\john.exe .\hash1.txt
.\john.exe --show .\hash1.txt
```

## 5. Validation and interpretation

| Check | Expected evidence | Publication handling |
| --- | --- | --- |
| John executable selected in Johnny | GUI settings screenshot | Add a sanitized screenshot later |
| JtR-compatible input loaded | Input file indicator, no sensitive string visible | Redact hash string |
| Audit completes | Sanitized Johnny result/status screenshot | Hide candidate password |
| PDF opens | Screenshot of non-sensitive training document | Only if reproduction permitted |

**Result:** The author reports completing the module. Exact attempt count, password value, elapsed time and screenshots are not available in the source materials reviewed for this repository.

## 6. Key takeaways

- A convenient interface can make password auditing accessible without changing the underlying attack model.
- Weak, predictable passwords may be recovered quickly with candidate-based testing.
- Password strength and document confidentiality should be assessed together.
- Locally handled audit data is generally preferable to submitting confidential documents to a third-party service.

**Source:** [John the Ripper](https://www.openwall.com/john/) · [Johnny GUI](https://openwall.info/wiki/john/johnny).
