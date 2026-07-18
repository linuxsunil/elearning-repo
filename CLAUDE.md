# CLAUDE.md — eLearning Authoring Repo

> This file is read by Claude Code and Claude AI agents working in this repository.
> It defines conventions, standards, and review protocols for all eLearning content and code.
> Do not delete or move this file. Update it when standards change.

---

## 1 — Project context

This repo contains source files for instructor-led training (ILT), eLearning modules, and blended learning programmes authored for corporate and professional-education clients.

**Primary authoring tools**: Articulate Rise 360, Storyline 360, Camtasia, Powtoon  
**LMS targets**: Docbo, Moodle, Cornerstone, generic SCORM-compliant LMS  
**Tracking standards supported**: SCORM 1.2, SCORM 2004 (3rd/4th edition), xAPI (Tin Can)  
**Accessibility target**: WCAG 2.1 Level AA  
**ID frameworks in use**: ADDIE, SAM, Bloom's Taxonomy (revised), Gagné's Nine Events  
**Audience**: Adult learners, professional / corporate context unless stated otherwise  
**Language**: British English by default; US English only when client spec says so  

---

## 2 — Repo conventions

### 2.1 Folder structure

```
/courses/          ← one subfolder per course (slug format)
/storyboards/      ← Word or Markdown storyboard source files
/scripts/          ← narration scripts (.md or .docx)
/assessments/      ← question banks and quiz configs (.json or .xlsx)
/xapi-statements/  ← xAPI statement templates and examples (.json)
/scorm-packages/   ← compiled SCORM ZIPs (never edit these directly)
/assets/           ← images, audio, video, fonts
/qa-reports/       ← QA checklist outputs and review logs
/.github/          ← PR templates and GitHub Actions workflows
```

### 2.2 File naming

- Use **kebab-case** always: `module-01-introduction.md` not `Module 1 Introduction.docx`
- Course slugs: `{client}-{course-name}-{version}` → `fractal-ml-foundations-v2`
- Storyboards: `{course-slug}-storyboard-{module-number}.md`
- Scripts: `{course-slug}-script-{module-number}.md`
- Assets: `{course-slug}-{asset-type}-{descriptor}.{ext}` → `fractal-ml-img-neural-network.png`
- SCORM packages: `{course-slug}-scorm{version}-{YYYY-MM-DD}.zip`

### 2.3 Storyboard file format

Storyboards are Markdown files. Each slide follows this template:

```markdown
## Slide {N} — {Title}

**Screen type**: [Title | Content | Interaction | Assessment | Summary]
**Narration**: [script text or reference to script file]
**On-screen text**: [text that appears on screen]
**Visual**: [description of graphic, animation, or media]
**Interaction**: [none | click-reveal | drag-drop | hotspot | scenario | quiz]
**Learning objective**: [mapped LO code, e.g. LO-01]
**xAPI verb**: [experienced | completed | answered | interacted | passed | failed]
**Notes for developer**: [any technical build notes]
```

### 2.4 Learning objective format

Objectives follow this structure:  
`LO-{module}-{number}: Learners will be able to {Bloom's action verb} {knowledge/skill} {condition/context}.`

Example:  
`LO-02-03: Learners will be able to distinguish between supervised and unsupervised learning given a real-world dataset description.`

---

## 3 — Instructional design standards

### 3.0 — Learning theory library

Claude must select and apply the most appropriate theory or model from this library based on content type, audience, and learning goal. Always state which theory is being applied and why in the module outline using the format:
`Theory applied: [Name] — Rationale: [one sentence]`

---

#### BEHAVIOURAL THEORIES
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 1 | Classical Conditioning (Pavlov) | Stimulus-response association | Attitude change, emotional response to content |
| 2 | Operant Conditioning (Skinner) | Behaviour shaped by reinforcement/punishment | Compliance training, habit formation, gamification |
| 3 | Social Learning Theory (Bandura) | Learning by observing others | Soft skills, leadership, safety behaviour modelling |
| 4 | Behaviour Modification | Systematic reinforcement to change behaviour | Performance improvement, onboarding |
| 5 | Programmed Instruction (Skinner) | Small steps, immediate feedback | Self-paced eLearning, drill and practice |

#### COGNITIVE THEORIES
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 6 | Cognitive Load Theory (Sweller) | Working memory is limited; reduce extraneous load | Complex technical training, data-heavy content |
| 7 | Schema Theory (Bartlett / Rumelhart) | New knowledge anchors to existing mental structures | Onboarding, concept mapping, analogies |
| 8 | Information Processing Theory (Atkinson & Shiffrin) | Sensory → working → long-term memory pipeline | Structuring content sequence, chunking |
| 9 | Dual Coding Theory (Paivio) | Verbal + visual channels process independently | Infographics, narrated slides, multimedia |
| 10 | Cognitive Theory of Multimedia Learning (Mayer) | Words + pictures better than words alone | eLearning slide design, video production |
| 11 | Elaboration Theory (Reigeluth) | Start simple, add complexity in layers | Curriculum sequencing, modular courses |
| 12 | Component Display Theory (Merrill) | Match instructional strategy to content type | Course architecture, content classification |
| 13 | Subsumption Theory (Ausubel) | Advance organisers bridge old and new knowledge | Module introductions, pre-assessments |
| 14 | Gestalt Theory | Learners perceive patterns as wholes | Visual design, layout, grouping of content |
| 15 | Metacognition Theory (Flavell) | Thinking about one's own thinking | Reflective practice, self-assessment |

#### CONSTRUCTIVIST THEORIES
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 16 | Constructivism (Piaget) | Learners build knowledge through experience | Scenario-based learning, problem solving |
| 17 | Social Constructivism (Vygotsky) | Learning is social; Zone of Proximal Development | Collaborative learning, cohort programmes |
| 18 | Discovery Learning (Bruner) | Learners construct understanding by exploring | Simulations, exploratory eLearning |
| 19 | Experiential Learning (Kolb) | Concrete experience → reflection → concept → experiment | Leadership development, ILT design |
| 20 | Situated Learning (Lave & Wenger) | Learning occurs in authentic contexts | On-the-job training, communities of practice |
| 21 | Anchored Instruction (CTGV) | Learning anchored in realistic problem scenarios | Case studies, video-based scenarios |
| 22 | Cognitive Apprenticeship (Collins et al.) | Expert models, then scaffolds, then fades support | Coaching, mentoring programmes |
| 23 | Problem-Based Learning (PBL) | Real problems drive knowledge acquisition | Medical, legal, technical professional training |
| 24 | Project-Based Learning | Extended real-world projects | Leadership, innovation, applied skills |
| 25 | Case-Based Reasoning | Prior cases guide solutions to new problems | Compliance, risk, sales training |

#### HUMANISTIC THEORIES
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 26 | Maslow's Hierarchy of Needs | Motivation follows a needs hierarchy | Learner motivation design, onboarding |
| 27 | Self-Determination Theory (Deci & Ryan) | Autonomy, competence, relatedness drive motivation | Engagement design, optional learning paths |
| 28 | Andragogy (Knowles) | Adults learn differently from children | All corporate eLearning — the baseline |
| 29 | Transformative Learning (Mezirow) | Learning changes frames of reference | DEI, leadership, culture change programmes |
| 30 | Heutagogy (Hase & Kenyon) | Self-determined learning beyond self-direction | Advanced professionals, expert learners |

#### CONNECTIVIST & NETWORKED THEORIES
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 31 | Connectivism (Siemens) | Learning is forming connections across networks | LXP design, social learning, AI-assisted learning |
| 32 | Communities of Practice (Wenger) | Learning happens through participation in communities | Knowledge management, peer learning |
| 33 | Distributed Cognition (Hutchins) | Cognition spread across people, tools, artefacts | Workflow learning, performance support tools |
| 34 | Actor-Network Theory (Latour) | Non-human actors (tools, systems) shape learning | Technology-enhanced learning design |

#### MOTIVATION & ENGAGEMENT MODELS
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 35 | ARCS Model (Keller) | Attention, Relevance, Confidence, Satisfaction | Motivation design across any course |
| 36 | Expectancy-Value Theory (Eccles) | Motivation = expectation of success × value of task | Goal-setting, learner buy-in |
| 37 | Flow Theory (Csikszentmihalyi) | Optimal engagement when challenge matches skill | Gamification, adaptive learning |
| 38 | Goal-Setting Theory (Locke & Latham) | Specific, challenging goals improve performance | Performance management, sales training |
| 39 | Attribution Theory (Weiner) | How learners explain success/failure affects motivation | Feedback design, resilience training |
| 40 | Self-Efficacy Theory (Bandura) | Belief in one's ability drives performance | Confidence-building, stretch assignments |

#### INSTRUCTIONAL DESIGN MODELS & LEARNING SCIENCE
| # | Theory / Model | Key Idea | Best used for |
|---|---|---|---|
| 41 | ADDIE | Analysis→Design→Development→Implementation→Evaluation | Standard ID project process |
| 42 | SAM (Allen) | Successive Approximation — agile, iterative ID | Rapid eLearning development |
| 43 | Gagné's Nine Events | Structured instructional events sequence | Module-level instructional planning |
| 44 | Bloom's Taxonomy (Revised) | Cognitive hierarchy of learning objectives | Objective writing, assessment design |
| 45 | Merrill's Principles of Instruction | Problem-centred, activation, demonstration, application, integration | Course architecture |
| 46 | 4C/ID Model (van Merriënboer) | Four Components for complex skill learning | Technical and professional skill training |
| 47 | Dick & Carey Model | Systems approach to instructional design | Large-scale curriculum development |
| 48 | Kirkpatrick Model | Four levels of training evaluation | Measuring training effectiveness |
| 49 | Phillips ROI Model | Adds ROI as a fifth evaluation level | Executive-level training justification |
| 50 | Action Mapping (Cathy Moore) | Business goal → behaviour → practice → content | Performance-focused eLearning |
| 51 | Universal Design for Learning (UDL) | Multiple means of representation, action, engagement | Inclusive learning design |
| 52 | Spaced Practice / Spacing Effect (Ebbinghaus) | Distributed practice beats massed practice | Microlearning, reinforcement campaigns |
| 53 | Interleaving | Mixing topics improves long-term retention | Assessment design, practice sequencing |
| 54 | Retrieval Practice (Testing Effect) | Recalling information strengthens memory | Quiz design, flashcards, knowledge checks |
| 55 | Worked Examples Effect | Studying solved problems before practising | Technical training, onboarding |
| 56 | Desirable Difficulties (Bjork) | Making learning harder improves long-term retention | Adaptive difficulty, varied practice |
| 57 | Cognitive Flexibility Theory (Spiro) | Ill-structured domains need multiple representations | Advanced topic instruction |
| 58 | Threshold Concepts (Meyer & Land) | Some concepts transform understanding irreversibly | Curriculum gateway design |
| 59 | Transfer-Appropriate Processing | Learning context should match performance context | Simulation, on-the-job training design |
| 60 | Cognitive Apprenticeship (Collins) | Model → coach → scaffold → fade | Expert skill transfer, mentoring |

---

### 3.1 Theory selection rules

Claude must follow this decision logic when selecting a theory for any module or course:

1. **Identify the performance gap type** — knowledge, skill, attitude, or motivation
2. **Identify the audience** — novice, intermediate, expert, adult professional
3. **Identify the context** — self-paced eLearning, ILT, blended, on-the-job, social
4. **Select the primary theory** most suited to those three factors
5. **Select a secondary theory** to address engagement or motivation if needed
6. **State the selection explicitly** in the module outline

Quick selection guide:

| If the goal is... | Primary theory | Secondary theory |
|---|---|---|
| Change a workplace behaviour | Operant Conditioning (2) | Behaviour Modification (4) |
| Teach a complex technical skill | Cognitive Load Theory (6) | 4C/ID Model (46) |
| Build soft skills through observation | Social Learning Theory (3) | Self-Efficacy (40) |
| Motivate disengaged learners | ARCS Model (35) | Self-Determination Theory (27) |
| Design for adult professionals | Andragogy (28) | Merrill's Principles (45) |
| Create scenario-based learning | Situated Learning (20) | Problem-Based Learning (23) |
| Design for long-term retention | Spaced Practice (52) | Retrieval Practice (54) |
| Teach in an AI/networked context | Connectivism (31) | Distributed Cognition (33) |
| Drive culture or mindset change | Transformative Learning (29) | Attribution Theory (39) |
| Measure training effectiveness | Kirkpatrick (48) | Phillips ROI (49) |
| Build learner confidence | Self-Efficacy (40) | ARCS Model (35) |
| Design inclusive learning | UDL (51) | Andragogy (28) |
| Advanced expert learners | Heutagogy (30) | Cognitive Flexibility (57) |

---

### 3.2 Bloom's Taxonomy verb map

Claude must use only **revised Bloom's** verbs. Match verbs to the correct cognitive level:

| Level | Verbs (use these) | Do not use |
|---|---|---|
| Remember | define, list, recall, recognise, identify, name | know, understand, learn |
| Understand | explain, describe, summarise, classify, compare | grasp, appreciate |
| Apply | use, demonstrate, solve, execute, implement | practise, try |
| Analyse | differentiate, examine, deconstruct, attribute | look at, break down |
| Evaluate | judge, critique, justify, recommend, assess | think about, consider |
| Create | design, construct, produce, devise, formulate | make, do |

### 3.3 Objective writing rules

- One observable, measurable action verb per objective
- Include the **condition** (given X) and **standard** (to Y level) where possible
- No compound objectives (no "and" connecting two verbs)
- Objectives must align to at least one assessment item

### 3.4 Gagné's Nine Events mapping

When writing a module outline, Claude must map content to Gagné's events where possible:

1. Gain attention — hook, scenario, surprising statistic
2. Inform learner of objectives — explicit LO display
3. Stimulate recall — prior knowledge activation
4. Present content — instruction slides
5. Provide learning guidance — worked examples, analogies
6. Elicit performance — practice activities
7. Provide feedback — corrective and elaborative feedback
8. Assess performance — summative quiz
9. Enhance retention and transfer — job aids, summary, scenario wrap-up

### 3.5 Assessment item rules

- Minimum 4 options for MCQ; one clearly correct answer
- Distractors must be plausible — no obviously wrong options
- Avoid negatively phrased stems ("which of the following is NOT...")
- Provide **corrective feedback** for every wrong answer (explain why it is wrong)
- Provide **elaborative feedback** for the correct answer (explain why it is right)
- Reading level: Flesch-Kincaid Grade 10 or below for narration; Grade 8 or below for on-screen text

---

## 4 — xAPI statement grammar

### 4.1 Required fields

Every xAPI statement in this repo must contain:

```json
{
  "actor": {
    "objectType": "Agent",
    "name": "Learner display name",
    "mbox": "mailto:learner@example.com"
  },
  "verb": {
    "id": "https://adlnet.gov/expapi/verbs/{verb}",
    "display": { "en-GB": "{verb}" }
  },
  "object": {
    "objectType": "Activity",
    "id": "https://{client-domain}/xapi/activities/{course-slug}/{activity-id}",
    "definition": {
      "name": { "en-GB": "{Activity name}" },
      "type": "https://adlnet.gov/expapi/activities/{type}"
    }
  }
}
```

### 4.2 Approved verb IDs

Use only ADL vocab verbs unless a cmi5 or custom verb is documented in the client brief:

| Action | Verb ID |
|---|---|
| Module started | `https://adlnet.gov/expapi/verbs/experienced` |
| Module completed | `https://adlnet.gov/expapi/verbs/completed` |
| Quiz answered | `https://adlnet.gov/expapi/verbs/answered` |
| Quiz passed | `https://adlnet.gov/expapi/verbs/passed` |
| Quiz failed | `https://adlnet.gov/expapi/verbs/failed` |
| Video played | `https://adlnet.gov/expapi/verbs/played` |
| Interaction clicked | `https://adlnet.gov/expapi/verbs/interacted` |
| Resource accessed | `https://adlnet.gov/expapi/verbs/accessed` |

### 4.3 Activity type IDs

```
Course:       https://adlnet.gov/expapi/activities/course
Module:       https://adlnet.gov/expapi/activities/module
Assessment:   https://adlnet.gov/expapi/activities/assessment
Question:     https://adlnet.gov/expapi/activities/question
Interaction:  https://adlnet.gov/expapi/activities/interaction
Video:        https://adlnet.gov/expapi/activities/media
```

### 4.4 Result object rules

- `score.scaled` must be a float between 0.0 and 1.0
- `success` must be a boolean
- `completion` must be a boolean
- `duration` must use ISO 8601 format (e.g. `PT1H23M45S`)

---

## 5 — SCORM compliance

### 5.1 SCORM 1.2 required CMI fields

Claude must ensure these are set in any SCORM 1.2 JavaScript:

```
cmi.core.student_id
cmi.core.student_name
cmi.core.lesson_status       ← "passed" | "failed" | "completed" | "incomplete" | "not attempted"
cmi.core.lesson_location
cmi.core.score.raw
cmi.core.score.min
cmi.core.score.max
cmi.core.session_time        ← format: HH:MM:SS.SS
```

### 5.2 SCORM 2004 required CMI fields

```
cmi.learner_id
cmi.learner_name
cmi.completion_status        ← "completed" | "incomplete" | "not attempted" | "unknown"
cmi.success_status           ← "passed" | "failed" | "unknown"
cmi.score.scaled             ← float -1.0 to 1.0
cmi.score.raw
cmi.score.min
cmi.score.max
cmi.session_time             ← ISO 8601 duration
cmi.location
```

### 5.3 imsmanifest.xml rules

- `<identifier>` at course and item level must be unique within the manifest
- `<title>` must match the course name in the brief
- `<adlcp:prerequisites>` used only if sequencing is required
- SCORM 2004: `<imsss:sequencing>` must be present if branching is used
- `<resource>` `href` must point to the actual launch file

### 5.4 What Claude must check in manifest diffs

- `schemaversion` matches the intended SCORM version
- `masteryScore` / `cmi.mastery_score` is set and matches the pass mark in the brief
- No broken `href` references
- `adlcp:scormtype` is `"sco"` for SCOs and `"asset"` for non-trackable resources

---

## 6 — Accessibility rules (WCAG 2.1 AA)

Claude must flag any content that violates these rules:

### 6.1 Images and graphics

- Every meaningful image must have descriptive `alt` text
- Decorative images must use `alt=""` (empty string, not missing)
- Alt text must describe the **meaning or function**, not the appearance
- Charts and diagrams must have a text alternative (caption or hidden description)

### 6.2 Video and audio

- All video must have closed captions (SRT or VTT format)
- Captions must be accurate (not auto-generated without review)
- Audio descriptions required for video where visual content carries meaning not in narration
- Do not rely on sound alone to convey information

### 6.3 Colour and contrast

- Text contrast ratio minimum: 4.5:1 (normal text), 3:1 (large text ≥ 18pt or 14pt bold)
- Do not use colour as the sole means of conveying information
- Interactive elements must have a visible focus indicator

### 6.4 Interactions and navigation

- All interactions must be keyboard-navigable
- Tab order must follow visual reading order
- No timed interactions unless the learner can pause, extend, or disable the timer
- Error messages must identify the field and describe how to fix the error

### 6.5 Reading level

- Narration: Flesch-Kincaid Grade 10 or below
- On-screen text: Grade 8 or below
- Define acronyms on first use in each module

---

## 7 — PR review protocol

When Claude is asked to review a PR in this repo, it must run through the following checklist and report findings under each heading. Flag issues as `BLOCKER`, `WARNING`, or `SUGGESTION`.

```
BLOCKER   — must be fixed before merge; breaks standards or compliance
WARNING   — should be fixed; degrades quality or learner experience
SUGGESTION — recommended improvement; not required
```

### 7.1 ID quality review

- [ ] Each slide has a mapped learning objective (LO code present)
- [ ] All objectives use correct revised Bloom's verbs at the stated cognitive level
- [ ] No compound objectives
- [ ] Assessment items align to stated LOs
- [ ] Feedback text is present for all assessment items (correct and incorrect)
- [ ] Gagné event mapping is present in module outline (if outline file changed)
- [ ] Reading level meets targets (narration ≤ FK Grade 10, on-screen ≤ FK Grade 8)

### 7.2 xAPI statement review

- [ ] All verb IDs use approved ADL vocab URIs
- [ ] Actor object contains `objectType`, `name`, and `mbox`
- [ ] Activity IDs follow the `https://{client-domain}/xapi/activities/{course-slug}/{id}` pattern
- [ ] Result `score.scaled` is within 0.0–1.0
- [ ] Duration uses ISO 8601 format
- [ ] No undefined custom verbs (must be documented if present)

### 7.3 SCORM compliance review

- [ ] Correct CMI fields are set for the target SCORM version
- [ ] `lesson_status` / `completion_status` logic handles all states
- [ ] `masteryScore` matches the pass mark in the brief
- [ ] imsmanifest identifiers are unique
- [ ] No broken `href` references in manifest
- [ ] `adlcp:scormtype` is correct for each resource

### 7.4 Accessibility review

- [ ] All images have alt text (or `alt=""` if decorative)
- [ ] Video files have a caption file referenced
- [ ] No colour-only information encoding
- [ ] No timed interactions without learner controls
- [ ] Tab order matches visual reading order (if interaction file changed)
- [ ] Contrast ratios documented or tool-verified

### 7.5 File and naming convention review

- [ ] All files use kebab-case
- [ ] File names follow the `{course-slug}-{type}-{descriptor}` pattern
- [ ] Storyboard slides use the required Markdown template
- [ ] LO codes are in `LO-{module}-{number}` format
- [ ] No files committed to `/scorm-packages/` that are not final ZIP exports

### 7.6 Content accuracy review (flag for SME if unsure)

- [ ] Technical claims can be verified against source material in repo
- [ ] Statistics and dates are cited (link or footnote in notes)
- [ ] No placeholder text (Lorem Ipsum, TBD, PLACEHOLDER) left in content
- [ ] Brand names and product names match client style guide

---

## 8 — Generation guardrails

When generating any content in this repo, Claude must:

**Always**
- Use British English unless client spec states otherwise
- Align every piece of content to a learning objective
- Apply revised Bloom's taxonomy — never "understand" or "know" as a verb
- Include feedback text for every assessment item
- Follow the storyboard slide template exactly

**Never**
- Invent statistics, citations, or data — flag as `[NEEDS SME VERIFICATION]`
- Generate assessment items with no plausible distractors
- Write objectives that are not measurable or observable
- Use passive voice in objectives ("will be taught", "will be shown")
- Commit to or recommend a SCORM version without checking the client brief
- Add interaction types not supported by the target authoring tool
- Generate audio scripts with sentences longer than 20 words (narration pacing)

**When uncertain**
- Insert `<!-- CLAUDE NOTE: {issue} — needs human review -->` in Markdown output
- Add `[FLAG: {reason}]` inline in narration scripts
- Never silently omit a required field — flag it instead

---

## 9 — Glossary

| Term | Meaning |
|---|---|
| ADDIE | Analysis, Design, Development, Implementation, Evaluation — ID process model (Theory #41) |
| CMI | Computer-Managed Instruction — data model fields in SCORM |
| cmi5 | xAPI profile for LMS-launched content (subset of xAPI) |
| FK Grade | Flesch-Kincaid Grade Level readability score |
| Gagné | Robert Gagné — Nine Events of Instruction framework |
| ILT | Instructor-Led Training |
| imsmanifest | XML file defining SCORM package structure |
| LMS | Learning Management System |
| LO | Learning Objective |
| MCQ | Multiple-Choice Question |
| SAM | Successive Approximation Model — agile ID process |
| SCO | Sharable Content Object — a trackable SCORM unit |
| SME | Subject Matter Expert |
| VILT | Virtual Instructor-Led Training |
| WCAG | Web Content Accessibility Guidelines |
| xAPI | Experience API (Tin Can) — learning data standard |
