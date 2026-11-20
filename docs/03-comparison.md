# Comparison — John/Johnny vs. Networkwalks browser tools

The two exercises use the same essential reasoning—prepare the PDF's audit data, test password candidates, verify access—but have different operational and confidentiality trade-offs.

| Dimension | W3-PM1: John + Johnny | W3-PM2: Networkwalks tools |
| --- | --- | --- |
| Main interface | Local Windows GUI controlling John | Web browser |
| Setup required | John + Johnny configuration | Little/no local installation |
| Password testing location | John operates locally | Browser-based service/workflow; processing details depend on provider |
| PDF extraction in the provided guide | An **external online extractor** is used | Networkwalks Hash Calculator |
| Ease of beginning | Moderate | High |
| Reproducibility | Strong with saved local configuration and tool versions | Depends on service availability and behavior |
| Confidentiality consideration | Local John processing helps, **but the guide's online extraction step still creates an upload risk** | Uploading training PDF data to an outside service introduces a data-sharing risk |
| Suitable for sensitive corporate documents? | Only with a fully approved and locally controlled extraction/auditing workflow | Not by default; requires organizational approval and validated service policies |
| Evidence to retain | Tool versions, GUI settings, sanitized audit result | Service date/version where available, sanitized result, validation |

## Security perspective

**No tool can guarantee recovery.** A successful exercise involving a deliberately weak training password demonstrates a particular risk scenario, not universal breakability. A robust passphrase, supported modern encryption settings and appropriate handling policies materially change the difficulty.

**Practical conclusion:** I found it useful to learn both methods. The GUI workflow reveals more of the tool configuration, while the web workflow reduces installation effort. When data sensitivity is a factor, I would favor a fully local, authorized assessment rather than uploading files to an unknown service.
