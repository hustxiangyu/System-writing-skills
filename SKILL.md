# Complete Guide to Top-Tier Computer Science Paper Writing Skills

> **Principle**: This skill system is distilled from paper-writing experience at top conferences and journals. In case of conflict or inconsistent detail between materials, the Markdown specification is the highest authority.

---

## Core Mental Models

1. **Primary Goal**: Make reviewers and readers understand — in the shortest possible time — what you did, why it matters, why it is hard, and why it works.
2. **Anticipate and Plug Holes**: Writing is a long-distance duel with the reviewer. Anticipate the objections a reader may raise (data bias, overhead, generalizability, etc.) and close those logical gaps in the main text beforehand.
3. **Reviewer Persona**: Assume the reviewer is a "broad-area peer" or "a second-year graduate student" — do not pile on obscure jargon without explanation, nor treat the reader as a group member who knows your internal implementation details.
4. **Align Intent with Working Memory**:
   - If you cannot write it clearly, you have not thought it through clearly.
   - Manage the reader's "working set": avoid uncontrolled synonym switching, keep paragraph structure modular, and repeat the core insight moderately.
5. **Explain, Not Describe**: "Why this design (trade-offs, motivation, root cause)" is always more important than "what the design looks like (first do A, then do B)".

---

## Module 1: Section-by-Section Breakdown and Practical Skills

### 1. Title
- **Core Formula**: `[Problem / Scenario] + [Core Method / Architecture] + [Value / Contribution]`
- **Key Points**:
  - Summarize the work precisely in one sentence, and coin a memorable system/model name where appropriate (e.g., `LineNet`, `DeepEye`, `Concordia`).
  - Avoid broad buzzwords; highlight the specific problem domain or novel mechanism.

---

### 2. Abstract (the full paper in miniature)
The abstract must close the loop strictly within 200–250 words:
- **What**: What problem is studied? Set the background and the core need.
- **Why**: Why are existing methods insufficient? Create the tension (limitations of prior solutions under new scenarios / new hardware / new trends).
- **How**: What is our core idea? Present the system's core design and 2–3 key mechanisms.
- **So What**: What did the experiments show? Give the most striking quantitative results (e.g., throughput up by $X\times$, latency down by $Y\%$).

---

### 3. Introduction (the narrative core that decides acceptance)
> **Note**: The Introduction almost single-handedly decides whether a paper is accepted. From the first line of code, keep reworking this story in the form of slides or a draft.

- **First sentence**: Get straight to the point — explain why this work is necessary, creating a sense of significance and urgency.
- **Create the tension**:
  - Identify the driving force: new hardware (NVM/RDMA/CXL), new scenarios (large models / Serverless / cloud-native), or new trends.
  - Derive the core challenge(s) from the tension. A good idea should focus on **one core problem**.
- **Lead to the design and the correspondence**:
  - Briefly present the designed system/method and show how it precisely breaks the above challenges (challenges can be elaborated in later detailed sections).
- **Loop back at the end**: In the second half of the introduction, return to the "Why" and emphasize the system-level significance of solving the problem (e.g., substantially improved GPU utilization, less distributed coordination).
- **Templated Contributions**:
  1. *Problem quantification / discovery*: We discover, quantify, and clearly define the XXX problem;
  2. *System / algorithm design*: We propose the XXX method/architecture, which solves the XXX problem theoretically / mechanistically;
  3. *Engineering implementation and experimental proof*: We implement a prototype on real hardware/systems; experiments show XXX improvement under XXX workloads.
- **Section mapping**: End the introduction with a short paragraph outlining how the rest of the paper is organized (Paper Organization).

---

### 4. Background & Motivation
- **Background**:
  - **Red line**: Never mix your own work or design into the background!
  - Define and explain the paper's core concepts and terminology in one place (avoid explaining a little in the Introduction and more elsewhere).
  - First give an overview of the subsections, then build them up step by step in an order a broad-area peer (second-year graduate student) can follow.
- **Motivation**:
  - Avoid dry preaching; argue with real traces, micro-benchmarks, or quantitative plots.
  - Analyze the **root cause** of why existing solutions fail, and derive your core **insight** naturally.

---

### 5. Design & Implementation
- **Principles before details**:
  - Do not dive straight into code or low-level details; first state the design principles and the overall architecture (Overview).
  - **Top-down structure**: First present the end-to-end workflow / architecture diagram and clarify the responsibility of each component; then drill into 2–3 core technical innovations in subsections.
- **Pseudocode vs. prose** (*Markdown rules take precedence*):
  - **Avoid pseudocode unless necessary; explain clearly with prose and figures**.
  - If an algorithm must be given, pair the pseudocode with an easy-to-follow example and a diagram to lower the reader's cognitive load.
- **Correspondence**:
  - Every design module must map one-to-one to a challenge raised in the Introduction, closing the loop.
- **Implementation**:
  - Keep it concise. Its purpose is to convince reviewers the system is solid and workable, removing doubts about engineering feasibility.

---

### 6. Evaluation
- **Questions first**: Open the experimental section with a short paragraph listing the research questions to answer (e.g., end-to-end speedup, per-module overhead, scalability).
- **Experimental dimensions**:
  1. *Effectiveness*: Benchmark against strong baselines on mainstream benchmarks and real workloads.
  2. *Ablation study*: Decompose the independent contribution of each technique to show not only that the system is good, but that the proposed mechanisms actually work.
  3. *Sensitivity and overhead*: Evaluate algorithmic overhead, parameter sensitivity, portability, and boundary conditions.
- **Data rigor**: Strictly distinguish data you measured yourself from data cited from others; avoid over-claiming in conclusions.

---

### 7. Related Work
- **Core positioning**: Explain **the essential difference between our method and others**, not write a second Background.
- **Scholarly posture**:
  - Fully acknowledge and praise the pioneering work of predecessors (the reviewer is very likely an author of that work), reflecting rigorous scholarship.
  - Make the contrast explicit: point out limitations of existing work under specific conditions, then highlight this work's distinctive contribution in addressing that limitation.
  - **Red line**: Never plagiarize or copy the related-work descriptions of other papers.

---

### 8. Limitation & Conclusion
- **The power of Limitation**:
  - No system is omnipotent (e.g., the RUM conjecture trade-off among read performance, write performance, and space).
  - After presenting the strengths, proactively and promptly state the limitations. This defuses the suspicion that you are hiding flaws, and clarifies that the flaw has limited impact on overall performance in the target scenario.
- **Conclusion**:
  - Summarize the core contributions with confidence, leaving reviewers sure the work is solid.
  - **Tone differs from the Introduction**: The Introduction targets readers who have not yet seen the details and focuses on story and motivation; the Conclusion targets readers who have read the whole paper and focuses on a high-level summary of the achieved effects and contributions.

---

## Module 2: Paragraph and Sentence Refinement

1. **Paragraph structure (claim-first)**:
   - **One paragraph, one central claim**.
   - Put the claim in the first sentence (Leading Sentence); the remaining sentences are evidence. Never drift from the claim.
   - Check every sentence in the paragraph and remove modifiers unrelated to the central claim.
2. **Sentence style and length**:
   - Shorter sentences are stronger; **keep one sentence under about 25 words**.
   - Avoid complex compound sentences; prefer simple sentences to express cause and logic.
   - Beware the low-level grammatical error of two predicate verbs in one sentence.
3. **Terminology consistency**:
   - Use one term consistently for one concept across the paper (e.g., do not mix message, packet, request, operation for the same thing).
   - Avoid fancy rare words; use standard, community-accepted expressions.
   - Be affirmative but objective; use absolute words (*must*, *unbeatable*) with care.
4. **Transitions**:
   - Logic first. If you cannot find a natural connective (*Therefore, In contrast, Specifically*) between two sentences, the leap of thought is too large and the order must be reworked.
   - Pronoun references must be clear; avoid vague "This" or "It" at the end of a sentence.

---

## Module 3: Visual Presentation and Layout

1. **Figures are king**:
   - Top-venue reviewers demand highly legible figures. Invest enough time in architecture and result figures so that "the core idea is clear from the figures and captions alone, without reading the body".
   - **Unified palette**: Use a consistent color family throughout (professional palettes are fine); avoid harsh high-saturation colors.
   - **Captions and spacing**: Tighten whitespace between image and caption, and between caption and body, to keep pages compact.
2. **Text layout aesthetics**:
   - **Last line of a paragraph**: Ideally the final line is longer than half the line width; avoid a single orphaned word or a tiny fragment on its own line.
   - **Emphasis**: Use bold and italics sparingly and deliberately; citations and figure labels may follow a consistent color/format convention.
   - **Formulas and symbols**: All math symbols and formulas must use standard notation; define symbols rigorously and keep them consistent throughout — never let the meaning of a symbol drift.

---

## Module 4: AI Assistance and Self-Check Principles

1. **Never let AI write the first draft**:
   - The first draft must be written by yourself, or filled in from a rigorous outline, expressing real design thinking and insight.
   - A typical AI failure mode is "big talk, platitudes, and falsehoods, lacking real design root causes and logical chains".
2. **The right way to use AI**:
   - Use it only for polishing, grammar correction (Grammarly / LLM checks), and verifying idiomatic academic phrases.
3. **Reader-view self-check (cache-flush re-read)**:
   - After writing a paragraph or a section, clear your background knowledge and re-read as an unprepared external reader.
   - Go sentence by sentence and ask two questions:
     - *What is my real intent in writing this sentence?*
     - *What information remains in the reader's mind? Will this cause ambiguity or misunderstanding?*
   - Once information is missing, immediately add the missing leading text in place.
