# Publish responsibly — checklist

Use this checklist before making the repository public. The current package contains no copied instructor task PDFs, protected training PDFs, raw PDF audit strings or recovered passwords.

- [x] Explain both Week 3 objectives and workflows in original language.
- [x] Attribute Networkwalks Academy and upstream tool authors.
- [x] Distinguish author-reported completion from independently observed evidence.
- [x] Exclude password-protected training PDFs and course handouts from the Git repository.
- [x] Exclude raw `$pdf$...` audit strings, recovered passwords, wordlists and John pot files.
- [ ] Add my **own** sanitized screenshots if I choose to publish them (see `assets/screenshots/README.md`).
- [ ] Review every screenshot for names, account IDs, file paths, browser profile details, tokens and passwords.
- [ ] Decide whether to add a license for my original prose; do not license Networkwalks' materials as my own.
- [ ] Add the repository description and optional topics on GitHub.

## Suggested GitHub repository details

**Name:** `Password-Security-Labs-Week3`  
**Description:** `Week 3 hands-on password security labs: PDF password auditing with John the Ripper, Johnny GUI, and Networkwalks browser tools.`  
**Topics:** `cybersecurity`, `ethical-hacking`, `john-the-ripper`, `password-security`, `pdf-security`, `security-labs`, `writeup`, `networkwalks`

## Publish from a local shell

1. Create an empty GitHub repository with the suggested name; do not pre-populate it with a README.
2. From inside this folder, run:

```bash
git init -b main
git add .
git commit -m "Document Week 3 PDF password security labs"
git remote add origin https://github.com/YOUR_USERNAME/Password-Security-Labs-Week3.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username. Authenticate through GitHub's normal sign-in/credential manager or an authorized integration; **never paste an access token or password into the repository**.
