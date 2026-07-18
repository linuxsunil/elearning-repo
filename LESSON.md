# LESSON.md — Lesson Design Standards & Templates

> **Version**: 1.0.0  
> **Last Updated**: 2026-01-18  
> **Applies To**: Course → Module → Topic → Lesson structure  
> **Related**: CLAUDE.md (project standards), ID_SKILL.md (methodology)

---

## 🎯 Overview

This document defines how to **design, structure, and template individual lessons** within our eLearning courses. It ensures:
- ✅ Consistent lesson experience across all courses
- ✅ Problem-based learning applied systematically
- ✅ Interaction patterns reusable and accessible
- ✅ Assessment aligned to learning objectives
- ✅ WCAG 2.1 AA compliance at lesson level

---

## 📐 Content Hierarchy

```
Course
├── Module (3-5 topics per module)
│   ├── Topic 1 (2-4 lessons per topic)
│   │   ├── Lesson 1.1
│   │   ├── Lesson 1.2
│   │   └── Lesson 1.3
│   ├── Topic 2
│   │   ├── Lesson 2.1
│   │   └── Lesson 2.2
│   └── Topic 3
│       └── Lesson 3.1
├── Module 2
└── Module 3
```

**Naming Convention**:
```
{course-slug}-{module}-{topic}-{lesson-number}.md

Example:
ai-ethics-v1-mod01-topic01-lesson01.md
```

---

## 🏗️ Lesson Types & Characteristics

### **1. Knowledge Lesson**
**Purpose**: Teach concepts, theories, or factual information  
**Primary Theory**: Schema Theory, Cognitive Load Theory  
**Typical Length**: 5-8 minutes  
**Structure**: Concept → Explanation → Application → Check  
**Assessment**: Knowledge check (ungraded)

**Example**:
```
Lesson: "What is Algorithmic Bias?"
- Hook: Real case (hiring tool rejecting qualified candidate)
- LO: Define algorithmic bias with examples
- Content: 2 chunks (definition + sources of bias)
- Interaction: Click-reveal (3 examples of bias)
- Check: Multiple choice with feedback
- Time: 6 minutes
```

---

### **2. Skill/Procedure Lesson**
**Purpose**: Teach how to DO something (step-by-step)  
**Primary Theory**: Cognitive Apprenticeship, Gagné's 9 Events  
**Typical Length**: 8-12 minutes  
**Structure**: Model → Guide → Practice → Feedback  
**Assessment**: Guided practice with corrective feedback

**Example**:
```
Lesson: "How to Review an AI Model for Bias"
- Hook: Your job (as manager, review this model)
- LO: Execute 5-step bias audit process
- Content: Model each step (video or animation)
- Interaction: Guided practice (apply each step)
- Feedback: Real-time, corrective
- Time: 10 minutes
```

---

### **3. Scenario/Decision Lesson**
**Purpose**: Apply knowledge to realistic workplace dilemmas  
**Primary Theory**: Situated Learning, Problem-Based Learning  
**Typical Length**: 8-15 minutes  
**Structure**: Dilemma → Explore → Decide → Consequence → Reflect  
**Assessment**: Decision consequence reveals learning

**Example**:
```
Lesson: "The Hiring Tool Dilemma"
- Hook: Scenario (you're Aria, hiring manager)
- LO: Identify ethical risks in AI systems
- Interaction: Branching decision (3 options)
- Feedback: Consequence for each choice
- Reflection: Why some choices better than others
- Time: 12 minutes
```

---

### **4. Simulation Lesson**
**Purpose**: Practice in safe, realistic environment  
**Primary Theory**: Experiential Learning, Constructivism  
**Typical Length**: 12-20 minutes  
**Structure**: Setup → Explore → Experiment → Reflect  
**Assessment**: Performance in simulation

**Example**:
```
Lesson: "Deploy an AI Model Responsibly"
- Hook: You're a data scientist deploying a model
- LO: Make responsible deployment decisions
- Interaction: Interactive simulation (5-7 decision points)
- Feedback: Simulation shows consequences in real-time
- Reflection: Debrief on choices made
- Time: 18 minutes
```

---

### **5. Assessment Lesson**
**Purpose**: Evaluate learner understanding (graded or ungraded)  
**Primary Theory**: Assessment Theory, Mastery Learning  
**Typical Length**: 10-15 minutes (not a typical lesson)  
**Structure**: Intro → Items → Feedback → Results  
**Assessment**: This IS the assessment

**Example**:
```
Lesson: "Module 1 Assessment"
- Intro: What you'll be tested on
- Items: 8 questions (MCQ, scenario, short-answer)
- Feedback: Per-item feedback (correct & incorrect paths)
- Results: Score, pass/fail, remediation path
- Time: 12 minutes
```

---

### **6. Reflective Lesson**
**Purpose**: Metacognition, self-assessment, application planning  
**Primary Theory**: Experiential Learning, Metacognition  
**Typical Length**: 5-10 minutes  
**Structure**: Prompt → Think → Write → Commit  
**Assessment**: Self-assessment (not graded)

**Example**:
```
Lesson: "Apply to Your Role"
- Prompt: How will you use this in your job?
- Think: Guided reflection (4 thought-starters)
- Write: Learner journals response
- Commit: Set action goal
- Time: 8 minutes
```

---

### **7. Capstone/Project Lesson**
**Purpose**: Synthesize & apply multiple concepts  
**Primary Theory**: Project-Based Learning, Constructivism  
**Typical Length**: 30+ minutes (or multi-lesson arc)  
**Structure**: Challenge → Create → Share → Reflect  
**Assessment**: Rubric-based project

**Example**:
```
Lesson: "Build Your AI Ethics Framework"
- Challenge: Design an ethics review process for your org
- Create: Develop framework (multi-step)
- Share: Present to peers
- Reflect: Peer feedback + self-assessment
- Time: 45 minutes (or 3 sessions)
```

---

## 🧠 Primary Structure: Problem-Based Learning (PBL)

### **When to Use PBL**
- Complex, real-world concepts
- Need learner engagement
- Want to build critical thinking
- Content lends itself to dilemmas/decisions

### **PBL Lesson Flow**

```
┌─────────────────────────────────────┐
│ 1. HOOK / PROBLEM PRESENTATION      │
│    (1-2 min)                        │
│                                     │
│ Real, authentic problem or dilemma  │
│ Learner has a role/stake            │
│ Creates curiosity & engagement      │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│ 2. LEARNING OBJECTIVES (Hidden)     │
│    (State upfront, but integrated)  │
│                                     │
│ LO-xx-yy: Learners will be able to │
│ [Bloom's verb] [concept/skill]      │
│ given [the problem context]         │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│ 3. GUIDED EXPLORATION               │
│    (3-5 min)                        │
│                                     │
│ Multiple approaches to understanding│
│ Hotspots, drag-drop, click-reveal   │
│ "What do you notice?" not "Here is" │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│ 4. LEARNER DECISION / CHOICE        │
│    (2-3 min)                        │
│                                     │
│ Branching scenario (2-4 options)    │
│ Each choice has consequence         │
│ No "correct" answer (reveal why)    │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│ 5. FEEDBACK & EXPLANATION           │
│    (2-3 min)                        │
│                                     │
│ Reveal consequence of each choice   │
│ Explain WHY (link to concept/theory)│
│ Normalize "learning from mistakes"  │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│ 6. REFLECTION & INTEGRATION         │
│    (1-2 min)                        │
│                                     │
│ Learner summarizes what they learned│
│ Apply to own role/context           │
│ Set action goal (optional)          │
└─────────────────────────────────────┘
```

**Total Time**: 10-15 minutes per lesson

---

## 📝 Lesson Template (Markdown Format)

Use this template for all lessons. Save as `{course-slug}-{mod}-{topic}-{lesson}.md`:

```markdown
# Lesson: [Descriptive Title]

**Lesson Code**: LES-{module}-{topic}-{number}  
**Module**: {module name}  
**Topic**: {topic name}  
**Lesson Type**: [Knowledge/Skill/Scenario/Simulation/Assessment/Reflective/Capstone]  
**Estimated Time**: {X} minutes  
**Learning Theory**: [Primary] - [rationale], [Secondary] - [rationale]

---

## Learning Objectives

LO-{mod}-{topic}-{num}: Learners will be able to {Bloom's verb} {knowledge/skill} 
{given the problem/context}.

*Link to Assessment*: Assessment Item X (question Y)

---

## Hook / Problem Presentation

**Screen Type**: Slide / Video / Interactive  
**Narration**: [Conversational, sets up the dilemma]  
**On-Screen Text**: [What learner sees]  
**Visual**: [Image/video/animation description]  
**Duration**: 1-2 minutes

**Purpose**: Hook engagement, establish role, create curiosity

---

## Guided Exploration

**Interaction Type**: [Click-reveal / Hotspot / Drag-drop]  
**Narration**: [Guide learner to notice key elements]  
**Elements**: 
- Element 1: [description]
- Element 2: [description]  
- Element 3: [description]

**Accessibility Considerations**: 
- [ ] Keyboard navigable (Tab to each element)
- [ ] Alt text for images (what the element is, not appearance)
- [ ] Focus indicator visible
- [ ] No color-only encoding

**Duration**: 3-5 minutes

---

## Learner Decision / Branching Scenario

**Interaction Type**: Branching Decision  
**Prompt**: [The decision the learner must make]  

**Option A: [Choice]**
- Consequence: [What happens]
- Why: [Explanation tied to learning objective]
- Learning: [What this teaches]

**Option B: [Choice]**
- Consequence: [What happens]
- Why: [Explanation tied to learning objective]
- Learning: [What this teaches]

**Option C: [Choice]**
- Consequence: [What happens]
- Why: [Explanation tied to learning objective]
- Learning: [What this teaches]

**Accessibility Considerations**:
- [ ] All options clearly readable (no color-only differentiation)
- [ ] Keyboard accessible (Tab through options)
- [ ] Screen reader announces option labels
- [ ] Consequences clear & text-based (not animation-only)

**Duration**: 2-3 minutes

---

## Feedback & Explanation

**Narration**: [Explain why each option was/wasn't effective]  
**Connection to LO**: [Link consequence back to learning objective]  
**Theory Application**: [How does this reinforce the learning theory?]

**Accessibility Considerations**:
- [ ] Explanation text provided (not video-only)
- [ ] Captions on any video
- [ ] Alt text on diagrams
- [ ] Plain language (no jargon without definition)

**Duration**: 2-3 minutes

---

## Reflection & Integration

**Reflection Prompt**: [Question for learner to answer]  
**Narration**: [Guide learner to think about application]

**Options**:
- [ ] Journaling (learner writes response)
- [ ] Multiple choice reflection question
- [ ] Self-assessment checklist
- [ ] Action goal setting

**Accessibility Considerations**:
- [ ] Text input provided (not speech-only)
- [ ] Character limit clear
- [ ] Auto-save feature (if journal)

**Duration**: 1-2 minutes

---

## Assessment / Knowledge Check

**Type**: [Ungraded Check / Graded Assessment / Self-Assessment]  
**Question Count**: {X}  
**Item Types**: [MCQ / Scenario / Short-answer / Other]

### Question 1
**Item Code**: Q-{mod}-{topic}-{num}-01  
**Stem**: [The question]  
**Options**: 
- A) [Correct answer with justification]
- B) [Plausible distractor - why it's wrong]
- C) [Plausible distractor - why it's wrong]
- D) [Plausible distractor - why it's wrong]

**Feedback**:
- Correct: "You got it! [Why this is correct]"
- A (if wrong): "[Explanation]"
- B (if wrong): "[Explanation]"
- C (if wrong): "[Explanation]"

**Maps to LO**: LO-{mod}-{topic}-{num}

[Repeat for each assessment item]

---

## Summary

**Learner Takeaway**: [One sentence summary of key learning]  
**Next Lesson**: [What's coming next and why it matters]

---

## Metadata

**Content Owner**: [Name]  
**Created Date**: {YYYY-MM-DD}  
**Last Revised**: {YYYY-MM-DD}  
**SME Verification**: [ ] Needed [ ] Complete  
**Accessibility Audit**: [ ] Needed [ ] Complete [ ] WCAG 2.1 AA Compliant  
**xAPI Mapping**: [ ] Needed [ ] Complete  
**SCORM Manifest Entry**: [ ] Needed [ ] Complete
```

---

## 🎨 Interaction Types & Templates

### **1. Click-Reveal**

**When to Use**:
- Reveal additional information progressively
- Reduce cognitive overload (don't show everything at once)
- Engage learner actively (click = engagement)
- Scenario exploration (click to learn more about situation)

**Template**:
```
Click-Reveal Hotspot

┌────────────────────────────────┐
│  [Background Image/Context]    │
│                                │
│  Click any icon to learn more: │
│                                │
│  🔵 [Icon 1: Label]            │
│  🟡 [Icon 2: Label]            │
│  🟢 [Icon 3: Label]            │
│                                │
│  → Revealed Text Below ←       │
│  [Content appears on click]    │
└────────────────────────────────┘
```

**Interaction Flow**:
1. Present situation (image + labels)
2. Learner clicks icon
3. Text reveals below or in tooltip
4. Learner can click multiple icons

**Accessibility Checklist**:
- [ ] All clickable areas keyboard navigable (Tab key)
- [ ] Focus indicator visible around each icon
- [ ] Icon has descriptive label (not just color)
- [ ] Alt text for background image
- [ ] Click handler also works on Enter/Space keys
- [ ] Screen reader announces all options
- [ ] No time limit on reveal
- [ ] Revealed text high contrast (4.5:1 minimum)

**Example (AI Ethics)**:
```
Icon 1: "Data Source"
  → "This AI was trained on hiring data from 2010-2015, 
     before diversity initiatives. The historical bias 
     is baked into the model."

Icon 2: "Job Criteria"
  → "The job description emphasizes 'aggressive sales 
     tactics' — a criterion where men were historically 
     overrepresented. The model learned this bias."

Icon 3: "Technical Glitch"
  → "Less likely. The model code was reviewed by engineers. 
     The issue is in the training data, not the algorithm."
```

---

### **2. Drag-Drop**

**When to Use**:
- Matching concepts to definitions
- Sequencing steps in order
- Categorizing items
- Kinesthetic engagement (movement = learning)

**Template**:
```
Drag-Drop Matching

Source (Draggable Items)        Target (Drop Zones)
┌──────────────────┐           ┌──────────────────┐
│ □ Bias           │           │ Definition A:    │
│ □ Fairness       │      →    │ [Drop zone]      │
│ □ Transparency   │           │                  │
│ □ Accountability │           │ Definition B:    │
└──────────────────┘           │ [Drop zone]      │
                               │                  │
                               │ Definition C:    │
                               │ [Drop zone]      │
                               │                  │
                               │ Definition D:    │
                               │ [Drop zone]      │
                               └──────────────────┘
```

**Interaction Flow**:
1. Learner sees items (left) and drop zones (right)
2. Drag item to drop zone
3. Feedback: "Correct!" or "Try again"
4. After all matches, reveal correct answers

**Accessibility Checklist**:
- [ ] Drag-drop keyboard accessible (Tab + arrow keys to select + Enter to drop)
- [ ] Alternative: Dropdown for each item (if native drag-drop difficult)
- [ ] Clear visual feedback (item highlights on hover, drop zone highlights on drag)
- [ ] Error messages clear (e.g., "Bias matches Definition A")
- [ ] No time limit
- [ ] Focus indicator on all elements
- [ ] Screen reader announces "Draggable item" and "Drop zone"
- [ ] Success message provided (audio + text)

**Example (AI Ethics)**:
```
Match terms to definitions:

Terms: Bias | Transparency | Accountability | Fairness

Definition A: "The ability to explain WHY an AI made a decision"
→ Transparency

Definition B: "Treating similar cases similarly, without discrimination"
→ Fairness

Definition C: "Systematic error favoring one group over another"
→ Bias

Definition D: "Taking responsibility for AI system outcomes"
→ Accountability
```

---

### **3. Branching Scenario**

**When to Use**:
- Decision-making (learner chooses path)
- Consequence exploration (see impact of choice)
- Scenario-based learning (Situated Learning)
- Building critical thinking

**Template**:
```
Branching Scenario

┌─────────────────────────────────────┐
│ SITUATION                           │
│ [Detailed scenario description]    │
│                                     │
│ YOU MUST DECIDE:                    │
│ [Decision prompt]                   │
│                                     │
│ Choose one:                         │
│ ◯ Option A: [Brief description]    │
│ ◯ Option B: [Brief description]    │
│ ◯ Option C: [Brief description]    │
└─────────────────────────────────────┘
         ↓ [Learner selects]
┌─────────────────────────────────────┐
│ CONSEQUENCE                         │
│ [What happens as result of choice]  │
│                                     │
│ ✓ Why this was/wasn't effective     │
│                                     │
│ [Next decision or conclusion]       │
└─────────────────────────────────────┘
```

**Interaction Flow**:
1. Present scenario
2. Offer 2-4 choices
3. Learner selects one
4. Show consequence
5. Explain why (link to learning objective)

**Accessibility Checklist**:
- [ ] Scenario text clear (not jargon-heavy)
- [ ] Radio buttons clearly labeled
- [ ] All options visible (no scrolling to see option C)
- [ ] Consequence provided in text (not animation-only)
- [ ] Color not sole indicator of choice/consequence
- [ ] No time limit on decision
- [ ] Keyboard navigable (Tab to radio, arrows to select, Enter to confirm)
- [ ] Screen reader announces "Choice: Option A selected"
- [ ] Consequence text same color contrast as scenario (4.5:1)
- [ ] Option to see all consequences (not locked after choice)

**Example (AI Ethics)**:
```
SITUATION: Your company just deployed a new AI hiring tool. 
Your manager shows you that it rejected a highly-qualified 
candidate. She asks why it happened.

YOU MUST DECIDE: What do you tell her?

◯ A) "The training data had bias from hiring patterns in 2010-2015.
     We need to retrain the model with more recent data."

◯ B) "There's a technical glitch. Let's have engineering fix the code."

◯ C) "It's just how AI works sometimes. We can't control it."

---

IF YOU CHOSE A:
✓ Correct approach. You identified the root cause (data bias) 
  and proposed a solution. This shows understanding of where bias 
  enters AI systems.

IF YOU CHOSE B:
✗ Less likely. The problem isn't technical — it's the training 
  data that learned historical hiring patterns. Fixing code won't 
  solve bias in the data.

IF YOU CHOSE C:
✗ Not true. Bias in AI is explainable and fixable. This attitude 
  avoids responsibility and doesn't solve the problem.
```

---

### **4. Hotspots (Image with Clickable Regions)**

**When to Use**:
- Learning parts of a system (diagram with labels)
- Annotating images (identify elements)
- Spatial learning (how things connect)
- Interactive diagrams

**Template**:
```
Interactive Hotspot Diagram

         [Large Image/Diagram]
         
         Click any part to learn:
         
         ⭕ Hotspot 1 → Label + Description
         ⭕ Hotspot 2 → Label + Description
         ⭕ Hotspot 3 → Label + Description
         
         [Info appears on click]
```

**Interaction Flow**:
1. Learner sees diagram with hotspot circles/indicators
2. Click hotspot
3. Label + description appears (in tooltip or below)
4. Click different hotspots to explore

**Accessibility Checklist**:
- [ ] Hotspot areas large enough (minimum 44x44 pixels)
- [ ] Each hotspot has descriptive label (e.g., "Algorithm component", not "Click here")
- [ ] Alt text for entire image: describes image purpose + hotspots
- [ ] Keyboard navigable (Tab to each hotspot, Enter to reveal)
- [ ] Focus indicator visible around each hotspot
- [ ] Descriptive text provided (not tooltip-only, readable by screen reader)
- [ ] Color not sole indicator (use icons + labels)
- [ ] Screen reader announces "Clickable: {label}"
- [ ] Info text 4.5:1 contrast minimum
- [ ] No time limit on exploration

**Example (AI Ethics — Model Pipeline)**:
```
[Image: AI Model Pipeline]

Hotspot 1: Data Collection
  → "Historical hiring records used to train the model. 
     If this data reflects past discrimination, the model 
     will learn and replicate it."

Hotspot 2: Model Training
  → "Algorithm learns patterns from the data. It's not 
     making decisions — it's finding patterns in training data."

Hotspot 3: Deployment
  → "Model now makes real hiring decisions. Any bias in 
     training data is now live, affecting real candidates."

Hotspot 4: Audit
  → "We check: Did the model reject candidates equally 
     across all demographics? If not, we have bias."
```

---

### **5. Multiple Choice with Feedback**

**When to Use**:
- Quick knowledge checks
- Assessment (graded)
- Reinforcing concepts
- Low cognitive load (select vs. construct)

**Template**:
```
Multiple Choice Item

Question: [Stem]
(Clarify what learner needs to do)

◯ A) [Correct answer with justification below]
◯ B) [Plausible distractor - why wrong below]
◯ C) [Plausible distractor - why wrong below]
◯ D) [Plausible distractor - why wrong below]

[After selection, feedback appears]

IF CORRECT: "Yes! [Explanation]"
IF INCORRECT: "Not quite. [Why this is wrong] [Correct answer]"
```

**Interaction Flow**:
1. Learner reads question stem
2. Selects one option
3. Feedback appears (correct or incorrect)
4. Can retake (for ungraded check) or move on (for assessment)

**Accessibility Checklist**:
- [ ] Question stem is clear (no double negatives)
- [ ] All options visible (no scrolling)
- [ ] Radio buttons clearly labeled
- [ ] Color not sole indicator (A/B/C letters + text)
- [ ] Feedback provided immediately
- [ ] Feedback text same size as question (readable)
- [ ] Feedback includes explanation (not just "wrong")
- [ ] Keyboard navigable (Tab, arrows, Enter)
- [ ] Screen reader announces "Question 1 of 5. Radio button A selected."
- [ ] Feedback text 4.5:1 contrast minimum
- [ ] No time limit (for ungraded checks)

**Example (AI Ethics)**:
```
Question: Which of the following is the PRIMARY source of bias 
in the hiring AI tool?

◯ A) The algorithm code is poorly written
   Feedback (if chosen): Not the main issue. The code was reviewed 
   by engineers. The problem is in the DATA it learned from.

◯ B) ✓ The training data reflects historical hiring patterns 
       where discrimination occurred
   Feedback (if correct): Exactly right. The model learned patterns 
   from historical data where certain groups were discriminated against. 
   When the model applies these learned patterns to new candidates, 
   it replicates the discrimination.

◯ C) The AI is intentionally programmed to discriminate
   Feedback (if chosen): Unlikely. AI doesn't have intent. But it can 
   replicate intent from the data it was trained on.

◯ D) AI is inherently biased and can never be fair
   Feedback (if chosen): Too pessimistic. Bias is a DATA problem, not 
   a technology problem. We can retrain the model with better data.
```

---

### **6. Fill-in-the-Blank**

**When to Use**:
- Vocabulary reinforcement
- Short-answer knowledge checks
- Completing definitions
- Sentence completion

**Template**:
```
Fill-in-the-Blank

Statement: "_______ is the systematic error that favors 
one group over another in an AI system."

[Text input field: _______________]

[Feedback on submit]

Correct Answer: "Bias"
Your Answer: "[What learner typed]"
Feedback: "Correct! Bias is a systematic error..."
```

**Interaction Flow**:
1. Learner reads statement with blank
2. Types answer in text field
3. Submits
4. Feedback shows correct answer + explanation

**Accessibility Checklist**:
- [ ] Blank clearly indicated (underline + label "Fill in: ___")
- [ ] Text input field has associated label
- [ ] Input field large enough to see typed text
- [ ] Feedback provided after submit (not real-time as typing)
- [ ] Case-insensitive matching (accept "BIAS" and "bias")
- [ ] Partial credit options (accept synonyms)
- [ ] Feedback explains correct answer (not just "yes/no")
- [ ] Keyboard only (no drag-drop needed)
- [ ] Screen reader announces "Text input: [label]"
- [ ] Text field has visible focus indicator
- [ ] Feedback text 4.5:1 contrast minimum

**Example (AI Ethics)**:
```
"_______ is the ability to explain why an AI system made a decision."

[Text input field]

Correct Answer: "Transparency"
Also accepted: "Model interpretability", "Explainability"

Feedback: "Correct! Transparency (or explainability) means we can 
understand and justify the AI's decisions. This is critical for 
accountability, especially in high-stakes decisions like hiring."
```

---

### **7. Sorting/Sequencing**

**When to Use**:
- Putting steps in order
- Prioritizing items (most to least important)
- Understanding prerequisites
- Process learning

**Template**:
```
Drag to Sequence

Correct Order:

Step 1: [Draggable item]
Step 2: [Draggable item]
Step 3: [Draggable item]
Step 4: [Draggable item]

[Learner reorders via drag-drop]

Feedback: "You got steps 1, 3, 4 correct. 
           Step 2 should come after step 3. Try again."
```

**Interaction Flow**:
1. Learner sees items in random order
2. Drags to reorder them
3. Submits
4. Feedback shows correct sequence
5. Explanation of why this order matters

**Accessibility Checklist**:
- [ ] Keyboard accessible (Tab + arrow keys to select + Enter to move)
- [ ] Clear visual feedback (item highlights when selected)
- [ ] Each item has descriptive text (not icon-only)
- [ ] Feedback specifies which steps are wrong
- [ ] Explanation of correct sequence provided
- [ ] Screen reader announces "Item 1: [description], draggable, in position 1"
- [ ] Color not sole indicator (use numbers + text)
- [ ] No time limit
- [ ] Visible focus indicator on each item

**Example (AI Ethics — Bias Audit Process)**:
```
Put these steps in the correct order for auditing an AI system:

Unordered:
- [ ] Review training data for demographic imbalances
- [ ] Collect performance metrics by demographic group
- [ ] Define fairness criteria for the domain
- [ ] Identify areas where fairness gaps exist
- [ ] Create remediation plan (retrain, adjust thresholds, etc.)

Correct Order:
1. Define fairness criteria for the domain
2. Collect performance metrics by demographic group
3. Review training data for demographic imbalances
4. Identify areas where fairness gaps exist
5. Create remediation plan

Explanation: You must first define WHAT FAIR MEANS in your context, 
then measure AGAINST that definition, then diagnose WHERE the problem 
is, then fix it.
```

---

### **8. Matching**

**When to Use**:
- Connect concepts to examples
- Match terms to definitions
- Pairing related items
- Vocabulary learning

**Template**:
```
Matching Exercise

Left Column (Items)          Right Column (Matches)
──────────────────          ───────────────────
1. Bias                      A) Treating similar cases similarly
2. Fairness                  B) Systematic error favoring one group
3. Transparency              C) Ability to explain AI decisions
4. Accountability            D) Taking responsibility for outcomes
```

**Interaction Flow**:
1. Learner sees items on left, definitions on right
2. Draws line or uses dropdown to match
3. Submits
4. Feedback shows correct matches

**Accessibility Checklist**:
- [ ] No drag-drop required (use dropdowns instead)
- [ ] Each item numbered (left) and lettered (right)
- [ ] Screen reader can access all items
- [ ] Clear instructions: "Match left items to right definitions"
- [ ] Feedback lists all correct matches: "1→B, 2→A, 3→C, 4→D"
- [ ] Explanation of why each match is correct
- [ ] No time limit
- [ ] High contrast between items and background (4.5:1)
- [ ] Keyboard navigable (Tab through dropdowns)

**Example (AI Ethics)**:
```
Match terms to definitions:

LEFT (Terms)               RIGHT (Definitions)
1. Algorithmic Bias  →     a) Systematic error in an AI model
2. Fairness          →     b) Treating like cases alike, without 
                              discrimination
3. Transparency      →     c) Explainability of AI decisions
4. Equity            →     d) Giving different treatment where 
                              differences matter
5. Accountability    →     e) Taking responsibility for AI outcomes

Feedback:
✓ 1→a (Algorithmic bias is systematic error)
✓ 2→b (Fairness means consistent, non-discriminatory treatment)
✓ 3→c (Transparency = explainability)
✓ 4→d (Equity recognizes when different groups need different support)
✓ 5→e (Accountability means owning the outcomes)
```

---

## ✅ Lesson-Level QA Checklist

Before finalizing any lesson, verify:

### **Instructional Design Quality**
- [ ] Learning objective clearly stated (Bloom's verb, measurable, realistic)
- [ ] Objective appears in lesson (not hidden)
- [ ] All interactions support the learning objective
- [ ] Assessment item(s) align directly to learning objective
- [ ] Feedback is constructive & explains the concept (not just "yes/no")
- [ ] Lesson follows chosen structure (PBL, Knowledge, Skill, Scenario, etc.)
- [ ] Pacing matches lesson type (5-8 min for Knowledge, 12-15 for Scenario)
- [ ] Interactions are purposeful (not decoration)
- [ ] Narration conversational (<20 words/sentence)

### **Content Accuracy & Clarity**
- [ ] All claims verified against sources
- [ ] Technical definitions accurate
- [ ] Examples relevant to learner context
- [ ] No placeholder text (Lorem Ipsum, TBD)
- [ ] Spelling & grammar checked
- [ ] British English spelling (colour, organisation, etc.)
- [ ] Acronyms defined on first use

### **Learning Theory Application**
- [ ] Primary theory selected & documented
- [ ] Secondary theory documented (if used)
- [ ] Design decisions traceable to theory rationale
- [ ] Theory application is explicit (not implicit)

### **Interaction Implementation**
- [ ] Interaction type matches its purpose (click-reveal for exploration, branching for decisions, etc.)
- [ ] All feedback provided (not just correct answers)
- [ ] Error messages constructive (not "Wrong")
- [ ] Consequences clear in branching scenarios
- [ ] No "tricky" questions (ambiguous stems)

### **Accessibility (WCAG 2.1 AA)**
- [ ] All images have alt text (function, not appearance)
- [ ] Color not sole information carrier (use labels, icons, text)
- [ ] Contrast ratio 4.5:1 minimum (text vs. background)
- [ ] All interactions keyboard navigable (Tab key works)
- [ ] Focus indicator visible on all interactive elements
- [ ] Interactive areas minimum 44x44 pixels
- [ ] No timed interactions (learner controls pace)
- [ ] Video has captions & audio description
- [ ] Text alternatives for all non-text content
- [ ] Form fields labeled (associated labels for screen readers)
- [ ] Reading level ≤ Grade 10 (Flesch-Kincaid)
- [ ] On-screen text ≤ Grade 8

### **SCORM & xAPI Compliance**
- [ ] xAPI verb appropriate for interaction (interacted, answered, etc.)
- [ ] xAPI statement structure valid (actor, verb, object, result)
- [ ] Activity ID follows standard pattern: https://[domain]/xapi/{course}/{lesson}
- [ ] SCORM completion/success status mapping defined
- [ ] CMI field mappings match SCORM version (1.2, 2004)

### **Assessment Item Quality** (if lesson includes assessment)
- [ ] Question stem is clear (no double negatives)
- [ ] Correct answer has clear justification
- [ ] Distractors are plausible (based on common misconceptions)
- [ ] Answer options parallel in structure
- [ ] No answer pattern (not always "C")
- [ ] Feedback for each option (correct & incorrect)
- [ ] Assessment maps to learning objective

### **Final Review**
- [ ] Lesson reviewed by SME (if needed)
- [ ] Lesson tested in target LMS (if applicable)
- [ ] All links functional
- [ ] File naming follows convention: {course}-{mod}-{topic}-{lesson}.md
- [ ] Metadata complete (owner, date, SME review status)
- [ ] Accessibility audit completed ✓ WCAG 2.1 AA compliant
- [ ] xAPI mapping complete
- [ ] SCORM manifest entry created (if applicable)

---

## 📊 Lesson Metadata

Every lesson must include:

```markdown
**Lesson Code**: LES-{mod}-{topic}-{num}
**Content Owner**: [Name]
**Created**: {YYYY-MM-DD}
**Last Revised**: {YYYY-MM-DD}
**Lesson Type**: [Knowledge/Skill/Scenario/etc.]
**Estimated Time**: {X} minutes
**Primary Theory**: [Name] - [Rationale]
**Secondary Theory**: [Name] - [Rationale]
**Assessment Items**: {Number of items}
**Interactions**: [List types used]
**SME Review Status**: ☐ Pending ☐ In Progress ☐ Complete
**Accessibility Audit**: ☐ Pending ☐ In Progress ☐ WCAG 2.1 AA ✓
**xAPI Mapping**: ☐ Pending ☐ Complete
**SCORM Entry**: ☐ Pending ☐ Complete
**Notes**: [Any special considerations]
```

---

## 🔗 How LESSON.md Integrates

### **Hierarchy**
```
CLAUDE.md (Project Standards)
    ↓
LESSON.md (Lesson Design Templates) ← You are here
    ↓
Individual Lesson Files
(e.g., ai-ethics-mod01-topic01-lesson01.md)
```

### **When Creating a New Lesson**
1. **Start with LESSON.md** — Choose lesson type & structure
2. **Use template** — Copy structure that matches lesson type
3. **Follow interaction guidelines** — Use appropriate interaction type
4. **Apply theory** — Select from learning theory library (in CLAUDE.md)
5. **Pass QA checklist** — Verify accessibility, alignment, quality
6. **Link to CLAUDE.md** — Ensure project standards met
7. **Reference ID_SKILL.md** — Connect to methodology

---

## 📚 Example Lessons (Full)

### **Example 1: Knowledge Lesson (5 min)**

**Title**: What is Algorithmic Bias?

[Full lesson using template, Hook → Exploration → Check → Summary]

---

### **Example 2: Scenario Lesson (12 min)**

**Title**: The Hiring Tool Dilemma

[Full lesson using PBL structure, Problem-based with branching decision]

---

### **Example 3: Skill Lesson (10 min)**

**Title**: How to Audit an AI System

[Full lesson using Model-Guide-Practice structure]

---

*[Full examples provided separately or on request]*

---

## 🚀 Getting Started

### **To Design a Lesson**
1. Answer: "What type of lesson is this?" (Knowledge, Skill, Scenario, etc.)
2. Choose structure from Section 2 (Lesson Types)
3. Use template from Section 3
4. Select interaction types from Section 4
5. Apply QA checklist from Section 5
6. Save as: `{course-slug}-{mod}-{topic}-{lesson}.md`

### **To Review a Lesson**
1. Check against QA checklist (Section 5)
2. Verify accessibility (WCAG 2.1 AA)
3. Confirm learning objective alignment
4. Test interactions for usability
5. Validate xAPI/SCORM mapping

### **To Teach Others**
1. Share this document
2. Point to lesson type they're creating (Section 2)
3. Guide to template (Section 3)
4. Reference interaction types (Section 4)
5. Use QA checklist for review

---

## 📖 Related Documents

- **CLAUDE.md** — Project standards, learning theory library, QA protocol
- **ID_SKILL.md** — Instructional design expertise, methodologies, use cases
- **Individual Lesson Files** — Actual lessons using this template

---

## 📝 Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0.0 | 2026-01-18 | Initial release — lesson types, PBL structure, 8 interaction templates, QA checklist |

---

**Last Updated**: 2026-01-18  
**Status**: ✅ Production Ready  
**Reviewed By**: Sunil Iyer  
**Next Review**: Q2 2026

---

## 🤝 Questions?

- **Which lesson type should I use?** → See Section 2 (Lesson Types)
- **How do I structure a problem-based lesson?** → See Section 3 (PBL Flow)
- **How do I make interactions accessible?** → See Section 4 (Interaction Types → Accessibility Checklist)
- **How do I know if my lesson is ready?** → See Section 5 (QA Checklist)
- **How does this relate to CLAUDE.md?** → See "How LESSON.md Integrates"
