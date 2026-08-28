# CSC 574 Project Instructions

## Project Location

The active project root is:

`/Users/home/Desktop/Home/Classes/CSC 574 | Computer Network Security/Project Study/slides.dwermke.com`

The course archive is under `csc574/`.

Professor-provided reference materials for creating study content belong in `course-reference/`. Treat their wording,
terminology, exam guidance, and learning expectations as authoritative for the study guides, exam questions, and flash
cards. This public repository publishes that folder, so do not add student work, credentials, or private course
materials unless the repository visibility is changed.

For exam-oriented content, follow `course-reference/exam-preparation-guidance.md`: the Learning Objectives on the
slides and exam page define testable material, while gray-line examples show possible Bloom-aligned task phrasing.

## Project Structure

- `course-reference/`: professor-provided guidance that informs study content but is not rendered in the site.
- `course-reference/exam-preparation-guidance.md`: professor guidance on Learning Objectives and Bloom-aligned exam tasks.
- `index.html`: GitHub Pages root entry point that redirects to `csc574/`.
- `csc574/index.html`: polished course archive and launcher.
- `csc574/lec01-introduction/`: Lecture 01 Slidev export.
- `csc574/lec02-fundamentals/`: Lecture 02 Slidev export.
- `csc574/lec03-intro-crypto/`: Lecture 03 Slidev export.
- `csc574/lec04-symmetric-crypto/`: Lecture 04 Slidev export.
- `csc574/study-notes/`: HTML study guides and examples.
- `csc574/flash-cards.html`: interactive flash-card page with independent Lecture 02, 03, and 04 sections.
- `csc574/exam-question-flash-cards.html`: exam-focused flash-card page with one card at a time and Previous/Next navigation.
- `csc574/exam questions/`: source Markdown files and rendered HTML pages for possible exam questions and the answer key.

The lecture order is Lecture 01, Lecture 02, Lecture 03, and Lecture 04.

The archive is study-guide-first. `csc574/index.html` presents Lecture 01 as a slide-deck card and Lectures 02–04 as
study-guide cards with compact `Open slides` links inside each card. The Flash Cards section links to
`csc574/flash-cards.html`, and Exam Questions remains below it. Keep Lecture 01 represented even though it does not
currently have a complete study guide.

The Flash Cards section contains two homepage links side by side: `Open Flash Cards` for lecture-specific cards and
`Exam Question Flash Cards` for exam-question practice. Keep both links compact and visible in that section.

## Running The Site

Preferred local serving command:

```bash
cd "/Users/home/Desktop/Home/Classes/CSC 574 | Computer Network Security/Project Study/slides.dwermke.com"
python3 -m http.server 4176
```

Open the archive at `http://localhost:4176/csc574/`.

Slidev exports use JavaScript modules, dynamic imports, and generated assets. Prefer HTTP serving when testing the complete site. The local archive cards intentionally link to the published working decks at `https://slides.dwermke.com/csc574/...` so the root `file://` archive remains useful without relying on local module permissions.

## GitHub Pages

The public repository is `https://github.com/DeviScript/csc574-study-guide`. GitHub Pages deploys the `main` branch
from `/(root)` at `https://deviscript.github.io/csc574-study-guide/`. The root `index.html` redirects visitors to the
course archive at `https://deviscript.github.io/csc574-study-guide/csc574/`; keep this entry point in place so the
GitHub Pages root URL does not return a 404.

After site changes, commit and push to `main`. GitHub Pages automatically redeploys the site; allow a few minutes for
the public URL to reflect a new commit.

## Slide Export Safety

The lecture folders are downloaded production exports, not Slidev source projects. Do not reformat, rename, or regenerate their hashed JavaScript, CSS, font, image, or markdown-module files unless explicitly requested.

If assets are missing, compare against the matching published deck at `https://slides.dwermke.com/csc574/<lecture>/` and preserve the existing directory layout. The generated bundles expect an `assets/` directory beside each lecture `index.html`.

## Study Guide Sources

Authoritative source files for Lecture 02 are outside this project tree:

- Transcript: `/Users/home/Desktop/CSC-ECE 574 CompNetSec - Lec02_ Fundamentals_Captions_English (United States).txt`
- Exam guide: `/Users/home/Desktop/Home/Classes/CSC 574 | Computer Network Security/Weeks/Week 01 - Aug 17-21/Notes/Exam Page | Outline Topics | Week 1/CSC_574_Fall_2026_Exam_Guide_Week_1.docx`
- Master guide with instructor-provided answers: `/Users/home/Desktop/Home/Classes/CSC 574 | Computer Network Security/Weeks/Week 01 - Aug 17-21/Study/Week 1 | Master Study Guide/CSC_574_Week_1_Master_Study_Guide.docx`

Use the `.txt` transcript for searchable spoken detail. Use the master guide as the authority for answer wording, course terminology, slide references, distinctions, formulas, and caveats. Do not replace instructor-specific answers with generic security explanations.

Transcripts supplied for the cryptography lectures:

- Lecture 03: `/Users/home/Desktop/CSC-ECE 574 CompNetSec - Lec03_ Intro Cryptography_Captions_English (United States).txt`
- Lecture 04: `/Users/home/Desktop/CSC-ECE 574 CompNetSec - Lec04_ Symmetric Cryptography_Captions_English (United States).txt`

Use these transcripts for exact professor wording, questions, examples, sidequests, exam hints, and lecture order. Treat the
exported slide decks as the source of truth for slide content and slide numbering.

## Lecture 02 Notes

The complete combined guide is:

`csc574/study-notes/lecture-02-security-fundamentals-complete.html`

It combines the slides, transcript, exam guide, and master guide. It should retain:

- The reference-style Learning objectives section: the seven objective bullets, followed directly by an Answers
  container organized by objective.
- Learning objective answers should be written as labeled definitions or explanations. For example, list
  Definition 1, Definition 2, and the Course definition separately, and keep Adversary, Trust, Threat model,
  Trust model, and Security model as separate labeled answers.
- Keep the Learning objectives answers container directly below the objective bullets. Do not put the detailed exam
  questions back into that section unless explicitly requested.
- Definitions from the provided answer key and slide references.
- Explicit subquestions `2A`, `2B`, `3A` through `3D`, `4A`, `4B`, `5A`, `5B`, `6A`, and `6B`.
- Each answer directly underneath its individual question or subquestion.
- The distinction that the five defense archetypes are prevention, deterrence, deflection, detection, and recovery.
- The broken server-room window classification as a vulnerability, with an intruder as a possible threat.
- The ATM operating system as trusted because the ATM depends on it, but not automatically trustworthy.
- The ransomware classification as modification plus interruption.
- Risk formulas `R = T x V x C` and simplified `R = P x C`.
- The principle of adequate protection and its cost/value tradeoff.

Do not put a separate answer key underneath the questions. If restructuring the review section, verify that every question has exactly one answer rendered directly below it and that explicit labels are not duplicated by automatic ordered-list numbering.

## Lecture 02 Slide-Note Layout

When updating `lecture-02-security-fundamentals-complete.html`:

- Use the actual exported slides from `csc574/lec02-fundamentals/` as the visual source. Do not replace slides with summaries or create a single-slide preview.
- Display slides in lecture order, one slide at a time. Use the slide-number dropdown to jump directly to slides and
  preserve click or keyboard advance behavior.
- The right-side `Lecture Notes` section must contain only `Slide Connection` and `Professor's Words`.
- Put answers to slide questions in a separate answer section directly underneath the slide, not inside the right-side Lecture Notes section. For Slide 14, format properties, adversaries, and mechanisms as labeled bullet lists when they contain multiple items.
- Use numbered question-and-answer formatting when a slide asks multiple questions.
- Map transcript content to the slide where the professor discusses it, not merely by approximate slide number. For example, Slide 9 asks “How would you define when a system is secure?”, while Slide 10 contains the follow-up questions “As expected by whom?”, “Under what conditions?”, and “When?”.
- Preserve the professor's exact transcript wording in `Professor's Words` whenever it is available. Keep any explanatory answer separate from the quotation.
- For Slide 14, answer all three ATM prompts: properties, adversaries and capabilities, and mechanisms. Place definitions in a separate section to the right of the numbered answers.
- Include the ATM reasoning chain when preparing exam material: asset/property -> adversary/capability -> vulnerability/threat -> attack classification -> defense.
- Keep the ATM model transferable to unfamiliar exam scenarios by including assets, participants, trust assumptions, TCB, adversaries, capabilities, vulnerabilities, threats, attacks, defenses, and operating conditions.
- Use the instructor's course terminology: the five defense archetypes are prevention, deterrence, deflection, detection, and recovery; an ATM operating system is trusted because the ATM depends on it, but it is not automatically trustworthy.
- Keep the major study sections collapsible and collapsed by default. The page navigation belongs across the top above the slide dropdown, and the main study layout should use the full available page width rather than reserve an unused sidebar column.

The original short example remains at `csc574/study-notes/lecture-02-security-fundamentals.html`; do not delete it unless asked.

## Lecture 03 and 04 Study Guides

The current study guides are:

- `csc574/study-notes/lecture-03-intro-cryptography.html` - 65-slide Lecture 03 deck.
- `csc574/study-notes/lecture-04-symmetric-cryptography.html` - 60-slide Lecture 04 deck.

When updating either page:

- Use the actual exported deck as the visual source: `csc574/lec03-intro-crypto/` or `csc574/lec04-symmetric-crypto/`.
- Match the Lecture 02 study-guide interaction pattern: page navigation across the top, a slide-number dropdown, one
  visible slide at a time, click or keyboard advance, and collapsed study sections below the viewer.
- Keep the full slide count and slide order: Lecture 03 has 65 slides and Lecture 04 has 60 slides.
- The `Lecture Notes` panel for the visible slide must remain separate from the slide and contain `Slide Connection` and
  `Professor's Words` where transcript wording is available.
- Keep the professor's transcript wording in the Lecture Notes when available. Do not present paraphrases as quotations.
- Relate transcript passages to the slide where the professor discusses that material; do not assign transcript content only by approximate slide number.
- Keep explanatory answers separate from the professor's quoted words. Do not add a standalone Exam Review section to
  the slide study-guide pages; exam preparation belongs on the dedicated Exam Questions and Flash Cards pages.
- For Lecture 03, preserve the distinctions between cryptography, cryptanalysis, cryptology, plaintext, ciphertext, encryption, decryption, keys, key space, symmetric/asymmetric cryptography, Kirchhoff's principle, one-time pads, perfect secrecy, information-theoretic security, computational security, and historical ciphers.
- For Lecture 04, preserve the distinctions between stream and block ciphers; pseudorandomness and one-time pads; IV/nonce reuse; ECB, CBC, and CTR; confusion and diffusion; DES, 3DES, and AES; padding; parallelism; random access; error propagation; and confidentiality versus integrity.
- Include the professor's exam-relevant caveats: do not roll your own cryptography, do not reuse one-time-pad or stream-cipher key material, do not use ECB for structured data, and remember that the covered modes do not provide integrity by default.
- Keep formulas and notation faithful to the lecture, using KaTeX or structured HTML when equations are shown.

## Flash Cards

The dedicated page is `csc574/flash-cards.html`. Keep three visible sections, one for each of Lectures 02, 03, and 04.
Each section should show one flash card at a time and have its own Previous and Next controls directly beneath the card.
Navigation must be independent per section, and clicking a card should reveal or hide its answer. Keep the Lecture 02
cards comprehensive enough to cover the Security Fundamentals study page, including threat modeling, STRIDE, ATM
analysis, trust, TCB, risk, and adequate protection. Keep the lecture-specific questions and answers grounded in the
corresponding study guide and lecture terminology. Use regular-weight answer text; use bullets or numbering for answers
that contain multiple items.

The dedicated exam-practice page is `csc574/exam-question-flash-cards.html`. It should present one exam-focused card at a
time with click or keyboard answer reveal and Previous/Next navigation. Keep the question-bank topics and answer wording
aligned with the standalone Exam Questions and Answer Key pages.

## Exam Questions Pages

The source files are `csc574/exam questions/CSC574_possible_exam_questions.md` and
`csc574/exam questions/CSC574_possible_exam_questions_answer_key.md`. Their rendered pages are the matching `.html`
files in the same directory. Preserve all question-bank and answer-key content when updating the presentation; update the
rendered pages from the Markdown sources when the source content changes.

## Validation

After editing HTML:

1. Run `get_errors` on every changed HTML file.
2. Open the changed page in a browser.
3. Check both desktop and narrow mobile layouts when changing presentation.
4. For study-guide changes, verify slide count/order, dropdown behavior, collapsed sections, responsive layout, and the
  absence of a standalone Exam Review section.
5. For Flash Cards changes, verify the three lecture sections, one visible card per section, independent Previous/Next
  controls, answer reveal behavior, and responsive layout.
6. For Exam Question Flash Cards changes, verify one visible card, Previous/Next navigation, answer reveal behavior,
  question-bank coverage, and responsive layout.

Do not modify the original transcript or supplied Word documents unless explicitly requested.
