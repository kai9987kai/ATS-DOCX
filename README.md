
# ATS-DOCX

**Modern protection against exploits on Applicant Tracking Software Systems.**

ATS-DOCX is a browser-based DOCX inspection, cleaning, and compliance lab for testing how resumes and documents behave inside Applicant Tracking Software pipelines. It focuses on detecting hidden or fragile document content, improving ATS readability, and producing cleaner, more transparent DOCX output.

The project includes both a safe compliance-focused cleaner and a controlled adversarial testing version for scanner hardening, exploit awareness, and defensive research.

---

## Overview

Applicant Tracking Systems often parse resumes by extracting text, reading internal DOCX XML, and interpreting formatting structures. Poor formatting, hidden content, unusual Unicode, metadata clutter, keyword stuffing, and obfuscated text can cause unreliable parsing or unfair scoring.

ATS-DOCX helps identify those risks by scanning DOCX files for ATS readability issues and giving a transparent cleanup workflow.

---

## Key Features

### DOCX Scanner

- Upload or drag-and-drop DOCX files
- Extract readable resume text
- Inspect internal DOCX structure
- Detect hidden or suspicious content patterns
- Flag zero-width characters and Unicode anomalies
- Highlight excessive keyword repetition
- Identify unusual metadata or fragile formatting
- Generate scan findings and compliance feedback
- Copy extracted text
- Export scan reports
- Maintain scan history during a session

### Cleaner & Transparent Optimizer

The safer `lite.html` version focuses on honest, visible, ATS-friendly document cleanup.

- Normalize Unicode
- Remove zero-width and fragile combining characters
- Strip hidden markup and metadata-like fragments
- Clean bullets, whitespace, tabs, repeated separators, and noisy symbols
- Reduce keyword stuffing while keeping readable meaning
- Compare resume content against a target job description
- Suggest missing visible keywords
- Add a transparent skills alignment section
- Add an optional audit appendix
- Export a clean DOCX
- Copy cleaned text
- Track an audit trail of cleanup actions

### Live Resume Metrics

- Word count
- Character count
- Estimated reading time
- Unique term count
- Top repeated term
- Keyword match analysis
- ATS hygiene checklist

### Session Tools

- Save and load session state
- Export session JSON
- Clear saved data
- Toggle light/dark theme
- Adjust scanner sensitivity
- Configure persistence settings
- Preview cleaned output and audit actions

### Defensive Research Mode

`Max-injectorversion.html` contains a more aggressive adversarial testing interface intended for controlled lab use only.

It can be used to test whether scanners, cleaners, or ATS-like parsers correctly detect risky document manipulation patterns such as:

- Unicode anomalies
- Hidden HTML-like fragments
- Invisible metadata-style content
- Semantic noise
- Obfuscation
- Keyword shuffling
- Multi-layered document structures
- Suspicious injected content patterns

This mode should be used only for defensive testing, validation, scanner hardening, and research on systems you own or are authorised to test.

---

## Project Files

```text
ATS-DOCX/
├── README.md
├── lite.html
├── Max-injectorversion.html
├── SECURITY.md
├── CODE_OF_CONDUCT.md
└── LICENSE
````

### `lite.html`

The main recommended version.

Use this for transparent ATS hygiene, resume cleanup, DOCX scanning, keyword comparison, report export, and clean DOCX generation.

### `Max-injectorversion.html`

Experimental adversarial lab version.

Use this only in controlled test environments to understand how exploit-like document patterns may appear and how detection systems can be improved.

### `SECURITY.md`

Security policy and vulnerability reporting information.

### `CODE_OF_CONDUCT.md`

Community standards for respectful contribution.

### `LICENSE`

MIT License.

---

## Getting Started

### Option 1: Open directly in a browser

Download or clone the repository, then open:

```text
lite.html
```

in a modern browser.

Recommended browsers:

* Chrome
* Edge
* Firefox
* Brave

### Option 2: Run with a local static server

```bash
git clone https://github.com/kai9987kai/ATS-DOCX.git
cd ATS-DOCX
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/lite.html
```

---

## Recommended Workflow

1. Open `lite.html`.
2. Upload a DOCX resume.
3. Run the DOCX scanner.
4. Review extracted text and scan findings.
5. Paste a target job description.
6. Compare keywords.
7. Clean and optimize the document.
8. Review the audit trail.
9. Export the cleaned DOCX.
10. Re-scan the exported document to confirm it is readable and transparent.

---

## ATS Hygiene Checklist

A strong ATS-readable document should:

* Use visible text only
* Avoid hidden keyword blocks
* Avoid white text tricks
* Avoid zero-width characters
* Avoid excessive keyword repetition
* Use simple headings
* Use standard sections such as:

  * Experience
  * Education
  * Skills
  * Projects
  * Certifications
* Keep formatting simple and readable
* Match job descriptions truthfully
* Export clean DOCX files with auditable content

---

## Use Cases

* Resume ATS readability testing
* DOCX parser resilience testing
* Resume formatting cleanup
* Hidden-content detection
* Unicode anomaly detection
* Keyword repetition analysis
* ATS compliance education
* Defensive research into document parsing edge cases
* Internal scanner QA
* Building safer applicant document pipelines

---

## Responsible Use

ATS-DOCX is designed for transparency, security testing, and document hygiene.

Do not use this project to misrepresent qualifications, deceive hiring systems, hide content from human reviewers, or manipulate real application pipelines. The safer cleaner workflow is designed to replace hidden manipulation with visible, truthful resume alignment.

The adversarial testing version exists so developers and researchers can understand risky patterns and improve defensive detection.

---

## Security Notes

DOCX files are structured archives that may contain XML, metadata, embedded content, formatting instructions, and unexpected text fragments. When testing unknown files:

* Use a trusted local environment
* Do not upload private resumes to untrusted third-party tools
* Avoid opening suspicious files in full office suites unless necessary
* Prefer browser-based inspection for initial analysis
* Review exported content before sharing
* Report vulnerabilities through the project security policy

---

## Limitations

ATS-DOCX is a browser-based research and compliance tool. It does not guarantee that every Applicant Tracking System will parse a document in the same way.

Different ATS platforms may vary in:

* DOCX parsing behavior
* Unicode normalization
* Metadata handling
* Keyword scoring
* Section recognition
* Table parsing
* Header/footer extraction
* PDF conversion behavior

Always validate important documents manually before submission.

---

## Roadmap Ideas

* Deeper DOCX XML tree viewer
* Side-by-side original vs cleaned comparison
* More detailed ATS risk scoring
* Exportable JSON scan schema
* Batch scanning mode
* PDF resume analysis
* Table and header/footer risk detection
* Resume section classifier
* Accessibility checks
* Local-only encrypted session storage
* More advanced keyword transparency reports
* Unit tests for known risky DOCX patterns
* GitHub Pages deployment guide
* Example safe test documents

---

## Contributing

Contributions are welcome.

Good contribution areas include:

* Scanner accuracy improvements
* Cleaner safety improvements
* UI and accessibility upgrades
* Documentation
* Test files
* Browser compatibility fixes
* Security hardening
* False-positive reduction
* Export format improvements

Before contributing, please read the code of conduct and keep changes aligned with the project’s defensive and transparent-use goals.

---

## Development Notes

This project is intentionally lightweight and browser-first.

Current project style:

* Static HTML
* Client-side interaction
* No required backend
* DOCX-focused scanning and export workflow
* Local testing friendly
* Easy to host on GitHub Pages or any static server

---

## License

This project is released under the MIT License.

See `LICENSE` for details.

---

## Disclaimer

ATS-DOCX is provided for educational, defensive, and research purposes. It is not legal, hiring, or career advice. Always use transparent and truthful application materials.

```
::contentReference[oaicite:1]{index=1}
```

[1]: https://github.com/kai9987kai/ATS-DOCX/tree/main "GitHub - kai9987kai/ATS-DOCX: Modern protection against exploits on Applicant Tracking Software Systems · GitHub"
