# magazine-writer

A Claude skill for writing, structuring, pitching, revising, and understanding professional magazine and newspaper feature journalism. Also handles short fiction for consumer magazines, which turns out to be a completely different discipline — something I didn't fully appreciate until I'd read six books on the subject.

Built under the TABARC-Code author identity. Part of a broader Claude skill ecosystem that uses YAML frontmatter, Dewey decimal classification, and bidirectional relationship contracts. This one doesn't have the Dewey stamp yet. It'll get it.

---

## What it actually does

There are a lot of "writing assistant" prompts out there. Most of them tell Claude to "write in a professional tone" and call it done. This is not that.

This skill is source-validated from seven books on magazine journalism craft — Hennessy, Hamilton, Ruberg, Peterson & Kesselman-Turkel, Sophie King, Fink — and covers the full professional workflow: from finding and sharpening an angle, through research and interviewing, structural modelling, prose craft, revision, pitching, and the freelance business mechanics that most writing guides ignore entirely. Because apparently teaching writers about kill fees and first serial rights is considered somebody else's problem.

It's one skill. Fifteen files. Fully cross-wired, so modules know about each other and hand off correctly. The master `SKILL.md` routes everything; the nine reference modules and five subskills carry the actual substance.

---

## Structure

```
magazine-writer/
├── SKILL.md                          ← master entry point; load this first
├── references/
│   ├── 01_subject_and_angle.md       ← angle development, news pegs, spin-off method
│   ├── 02_article_structure.md       ← editorial hierarchy, nut graf, article templates
│   ├── 03_prose_and_voice.md         ← register, sentences, style modes, SEO, headlines
│   ├── 04_pitch_and_query.md         ← query letters, slot targeting, pitch log
│   ├── 05_publication_standards.md   ← publication DNA, register calibration
│   ├── 06_kaizen_improvement.md      ← improvement loop, personal standards doc
│   ├── 07_freelance_business.md      ← rights, contracts, kill fees, rates, media law
│   ├── 08_story_structure_models.md  ← Kebab, Accordion, Five-Box, Diamond, Post-it method
│   └── 09_writer_development.md      ← specialisation, brand, editor relationships, resilience
└── subskills/
    ├── article-type-master/           ← profiles, investigations, how-tos, roundups, columns...
    ├── leads-and-endings/             ← full lead taxonomy, ending types, bookend technique
    ├── research-and-interviewing/     ← source strategy, interview conduct, fact-checking
    ├── revision-and-self-editing/     ← three-level revision, reading-aloud protocol
    └── short-fiction/                 ← magazine short stories; separate workflow entirely
```

Each file ends with a `→ Where this module leads` section that routes to the next relevant module based on what the writer needs. This was added after an audit revealed thirteen of fifteen files had zero awareness of each other. That was fixed.

---

## What's in each module

**Module 01 — Subject and Angle.** The angle is not the subject. "Climate change" is a subject. "Why your local council is sitting on a £4m green energy grant it cannot spend" is an angle. This module covers how to get from one to the other, plus news pegs, evergreen calibration, and the spin-off method for extracting multiple pitches from one research session.

**Module 02 — Article Structure.** The editorial hierarchy: lead, nut graf, body, ending. Article type templates. Advanced nut graf technique including the pre-draft approach (write the nut before the draft — it clarifies the angle before you've committed to 2,000 words). Reviews, Q&As, and listicles are in here too because they kept coming up and the original skill didn't cover them.

**Module 03 — Prose and Voice.** Register calibration by publication type. Sentence craft, active voice, verb strength, transitions, scene-setting, quote handling. The tabloid toolkit — developed for mass-market publications but applicable everywhere, with appropriate calibration. Four style modes: description, narration, exposition, argument. Headlines for print and digital. SEO essentials including a note on AI summaries in 2025–26 search, because that's now the landscape.

**Module 04 — Pitch and Query.** Query letter anatomy. The pitch as writing sample (which it is — editors use it to assess whether you can write the piece, not just whether you have a good idea). Cold vs warm pitching. Slot targeting. International pitching. The pitch log, which is basically the freelance equivalent of a CRM and is equally neglected by the people who most need it.

**Module 05 — Publication Standards.** Publication DNA and how to read it. Register calibration by type: broadsheet supplement, consumer, trade, literary, specialist. The quality checklist before filing.

**Module 06 — Kaizen: Continuous Improvement.** The improvement loop applied to writing craft. The four pillars — continuous improvement, error-proofing, standardised work, just-in-time — translated into writing practice. Personal standards document template. The compound effect table showing what 1% improvement per piece accumulates to over fifty pieces. Also has a section on the writer's inner life — imposter syndrome, catastrophising rejection, confusing busyness with productivity — because Kaizen is self-improvement, not just task improvement.

**Module 07 — The Freelance Business.** Rights and copyright. Kill fees. Payment on acceptance vs publication. Indemnity clauses. Rates and negotiation. Media law basics (libel, privacy, recording). Record-keeping for legal protection. This module exists because almost no writing craft book covers it adequately, and writers consistently sign contracts they shouldn't.

**Module 08 — Story Structure Models.** The seven named structures: Inverted Pyramid, Kebab/Circle, Accordion, Hourglass, Rick Bragg Five-Box, Diamond, Braided Narrative. When to use each. The Post-it storyboard method (Line Vaaben / Poynter) for structuring longform pieces before drafting. Structural diagnostic questions. Decision guide.

**Module 09 — Writer Development.** Specialisation: identifying it, building it, defending it. Personal brand. Editor relationships. Writer's block — seven causes with specific solutions, because "writer's block" isn't one thing and treating it as one thing is why the generic advice doesn't help. Long-term practice. The Kaizen commitment applied at career level.

**Subskill: Article Type Master.** Profiles, roundups, how-tos, investigations/alarmers, narrative features, personal experience, surveys, opinion columns, travel, interview features, children's magazine writing, shorts, sidebars, templated writing. Each with its own structural logic, research requirements, common failures, and the specific reader contract it must fulfil.

**Subskill: Leads and Endings.** The full lead taxonomy — anecdote, declarative, scene-setting, contrast, question, "best shot," circular/suspended — with construction requirements for each. The three-part intro structure (Hennessy). Anecdote construction and placement rules. All ending types. The bookend technique. Failure catalogues for both.

**Subskill: Research and Interviewing.** The research mindset and four-step strategy. Finding and evaluating sources. Interview preparation, conduct, and the "sensory data" imperative for face-to-face work. Handling evasive, over-prepared, and hostile sources. E-mail interviews — when they're actually the better choice. The fact-check gate. Organising research before drafting.

**Subskill: Revision and Self-Editing.** Three levels: macro (structure and argument), mid (sections, pacing, transitions), micro (sentence, word, rhythm). Reading aloud protocol. The final 10% cut. Self-editing checklist. Rewriting vs editing — a distinction that saves a lot of wasted effort.

**Subskill: Short Fiction.** Market identification and how to read a magazine's fiction slot. Story structure for the short form. The twist ending — what makes it fair vs what makes it a cheat. Characterisation under word-count pressure. Dialogue. First lines. Submission strategy. This is structurally a separate workflow from feature journalism; it loads independently.

---

## Kaizen

The skill applies Kaizen throughout — not as a branding choice but because the improvement loop is genuinely how craft develops. Every module feeds into the improvement tracking in Module 06. The personal standards document template in that module is worth using regardless of everything else.

The principle: name one specific weakness before every draft. Fix it. Document what worked. Repeat. Small, specific improvements compound. After fifty pieces at 1% improvement each, the work is unrecognisable.

---

## Technical notes

- One `SKILL.md` at root — the system requires exactly one
- YAML frontmatter: `name`, `author`, `version`, `description` (under 1024 characters — ask me how I know)
- All cross-references use relative paths from the skill root
- Every file ends with a `→ Where this module leads` section routing to the next relevant module
- UK English throughout
- ~4,100 lines across 15 files

---

## What it doesn't do

It doesn't write the articles for you, although it'll help you draft them. It doesn't replace reading the target publication before pitching. It doesn't know your editor's current editorial calendar or what they spiked last month. It can't fact-check against primary sources on your behalf — that's still your job.

It also doesn't turn bad ideas into good ones. It does help you recognise which is which.

---

## Author

**TABARC-Code** — technical and editorial skills, part of a wider Claude skill ecosystem.

---

*v4.0 — built from seven source texts, three audit passes, one structural rewire, and two validator errors that seemed obvious in retrospect.*
