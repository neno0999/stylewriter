---
name: stylewriter
description: "Writing style analyzer and cloner for any author. Use this skill whenever a user wants to: replicate someone's writing style, analyze a writing sample to extract style DNA, generate content that sounds like a specific person, clone a voice for social media / articles / blogs, or use a preset writing style. Trigger for phrases like 'write in my style', 'clone this writing style', 'make it sound like X', 'analyze my writing', 'write a post that sounds like me', 'use [person] style', or any request that combines style + content generation. Always use this skill before generating style-matched content — never guess at style from a name alone."
---

# StyleWriter

A skill for analyzing and replicating any writing style with precision. Supports two modes:

- **Mode A — Analyze**: User provides a writing sample → extract Style DNA → generate content in that style
- **Mode B — Preset**: User selects a built-in style preset → generate content immediately

---

## WORKFLOW

### Step 0 — Detect Mode

If the user provides a writing sample or says "analyze my style / clone this" → go to **Mode A**.
If the user says "use [preset name]" or asks for a named style → go to **Mode B**.
If unclear, ask: *"Do you want to provide a writing sample to clone, or use a preset style?"*

---

## MODE A — ANALYZE & CLONE

### Step 1 — Request Sample

Ask the user to provide a writing sample (minimum 300–500 words). The sample should:
- Be written by a single author
- Contain natural paragraphs (not just lists)
- Represent the author's typical tone and structure
- Be from the platform they want to write for (Threads post, LinkedIn article, blog, etc.)

*Do not start analysis until the sample is provided.*

---

### Step 2 — Extract Style DNA

Once the sample is provided, analyze it across these 7 dimensions:

**1. Sentence Structure**
- Average sentence length (words per sentence)
- Ratio of short vs long sentences
- Use of compound/complex sentences

**2. Rhythm & Flow**
- Sentence pacing patterns
- Variation between short and long sentences
- Presence of rhetorical beats or emphasis

**3. Punctuation Profile**
- Frequency per 100 words: commas, periods, dashes, ellipses, parentheses, colons
- Signature punctuation habits (e.g., heavy dash user, minimal comma user)

**4. Vocabulary Complexity**
- % simple vocabulary vs advanced/technical vocabulary
- Typical word length
- Presence of jargon or domain-specific language
- Use of colloquialisms or informal phrasing

**5. Paragraph Structure**
- Average sentences per paragraph
- Pattern: short bursts vs dense blocks vs mixed

**6. Tone & Voice**
- Tone type: formal / conversational / persuasive / analytical / narrative / authoritative
- How the tone is achieved (word choice, sentence length, etc.)
- First person vs second person vs third person tendency

**7. Signature Style Markers**
- Recurring phrases or sentence openers
- Use of rhetorical questions
- Metaphors or analogies
- Formatting tendencies (bullets, line breaks, headers)
- What the writer *never* does (avoidances)

---

### Step 3 — Present Style DNA

Output a clean Style DNA card:

```
STYLE DNA — [Author/Source Label]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

SENTENCE STRUCTURE
• Avg length: X words/sentence
• Short/long ratio: X:X
• Compound sentences: rare / occasional / frequent

RHYTHM
• Pacing: [describe]
• Beat pattern: [describe]

PUNCTUATION PROFILE
• Commas: X per 100 words
• Dashes: X | Ellipses: X | Colons: X
• Signature habit: [describe]

VOCABULARY
• Simplicity: X% simple / X% advanced
• Domain: [general / technical / niche]
• Colloquial: yes / no

PARAGRAPH STRUCTURE
• Avg sentences/paragraph: X
• Pattern: [short bursts / dense blocks / mixed]

TONE & VOICE
• Type: [formal / conversational / etc.]
• POV: [first / second / third person]
• How tone is achieved: [describe]

SIGNATURE MARKERS
• Recurring patterns: [list]
• What this writer NEVER does: [list]

REPLICATION RULES
[3–5 clear rules a writer must follow to match this style]
```

---

### Step 4 — Request Topic & Platform

Ask:
1. What topic do you want to write about?
2. Which platform? (Threads / LinkedIn / Blog / Other)

---

### Step 5 — Generate Style-Matched Content

Write content on the given topic matching the Style DNA exactly:
- Match sentence length distribution
- Match punctuation density
- Match paragraph structure
- Match vocabulary complexity
- Apply tone markers
- Apply signature stylistic fingerprints
- Respect the avoidances

**Platform-specific length targets:**
- Threads: 1–5 short paragraphs, max 500 chars per post, conversational
- LinkedIn article: 600–1200 words, structured, professional opener
- Blog post: 800–2000 words, SEO-aware, clear H2 structure
- Social caption (generic): 100–250 words

---

### Step 6 — Validate the Clone

Present a comparison table:

| Metric | Original Sample | Generated Text |
|---|---|---|
| Avg sentence length | | |
| Short/long ratio | | |
| Paragraph structure | | |
| Vocabulary complexity | | |
| Punctuation density | | |

Calculate a **Style Match Accuracy (%)** based on metric similarity.
Note briefly where the match succeeds or deviates.

---

### Step 7 — Refinement

Ask the user:
- Refine the cloned style for higher accuracy?
- Generate another piece with the same style?
- Save this Style DNA for future use (as a named preset)?
- Analyze a different writing style?

---

## MODE B — PRESET STYLES

Use these built-in presets when the user requests a named style. Each preset includes replication rules ready to apply immediately.

---

### PRESET: Conversational Expert
*Best for: Threads, casual LinkedIn, newsletter*
- Short sentences. Avg 10–14 words.
- Speaks directly to reader (you/your).
- Uses rhetorical questions to create tension.
- No jargon unless explained immediately.
- Paragraphs: 1–2 sentences max.
- Avoids: passive voice, corporate phrases, excessive hedging.

---

### PRESET: Analytical Practitioner
*Best for: LinkedIn articles, blog posts*
- Medium-long sentences. Avg 15–20 words.
- Leads with observation, not conclusion.
- Uses specific numbers and field examples.
- First person but not confessional.
- Paragraphs: 3–4 sentences, logically connected.
- Avoids: hype words, empty motivational phrases, self-promotion.

---

### PRESET: Minimal Storyteller
*Best for: Threads, Instagram, short blog*
- Very short sentences. Avg 6–10 words.
- Heavy use of white space and line breaks.
- Builds tension through pacing.
- Concrete sensory details, not abstractions.
- Paragraphs: 1 sentence only.
- Avoids: explanation, over-qualification, filler words.

---

### PRESET: Direct Authority
*Best for: LinkedIn, Twitter/X, announcements*
- Declarative sentences. No hedging.
- States the point in sentence one.
- Uses data or credentials to anchor claims.
- Formal but not stiff.
- Paragraphs: 2–3 sentences.
- Avoids: questions, softeners ("maybe", "perhaps"), long intros.

---

### PRESET: Warm Educator
*Best for: Blog, explainer threads, educational content*
- Medium sentences. Avg 12–16 words.
- Uses analogies and relatable examples.
- Anticipates reader confusion and addresses it.
- Inclusive tone (we/us/you).
- Paragraphs: 3–5 sentences.
- Avoids: condescension, unexplained jargon, dense walls of text.

---

## ADDING CUSTOM PRESETS

Users or repo maintainers can add presets by following this format in SKILL.md:

```
### PRESET: [Name]
*Best for: [platforms]*
- [Rule 1]
- [Rule 2]
- [Rule 3]
- Avoids: [list]
```

To contribute a preset based on a real writing sample, run Mode A → Step 3 first, then convert the Style DNA card into preset format.

---

## QUALITY RULES (apply to all output)

1. **Never write "as a [style name] writer..."** — just write in the style
2. **Never explain what you're doing** — output the content directly
3. **Match platform conventions** — Threads ≠ LinkedIn ≠ Blog
4. **Preserve avoidances strictly** — what a writer doesn't do is as important as what they do
5. **When in doubt, go shorter** — most social content fails by being too long, not too short