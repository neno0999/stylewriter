# StyleWriter

> A Claude skill for analyzing and replicating any writing style — for Threads, LinkedIn, blogs, and beyond.

StyleWriter extracts the "Style DNA" of any writing sample and uses it to generate new content that sounds authentically like the original author. Works across all major content platforms.

---

## What It Does

**Mode A — Analyze & Clone**
Paste any writing sample → StyleWriter extracts a full Style DNA (sentence structure, rhythm, punctuation, vocabulary, tone, signature markers) → generates new content in that exact style.

**Mode B — Preset Styles**
Skip the analysis. Pick a built-in preset and start writing immediately.

---

## Preset Styles Included

| Preset | Best For |
|---|---|
| Conversational Expert | Threads, casual LinkedIn, newsletters |
| Analytical Practitioner | LinkedIn articles, blog posts |
| Minimal Storyteller | Threads, Instagram, short-form |
| Direct Authority | LinkedIn, announcements, X/Twitter |
| Warm Educator | Blog, explainer threads, educational content |

---

## How to Install

### Option 1 — Install `.skill` file (Claude Desktop / Claude Code)
1. Download `stylewriter.skill` from the [Releases](../../releases) page
2. Open Claude → Settings → Skills → Install from file
3. Select `stylewriter.skill`

### Option 2 — Manual install via `SKILL.md`
1. Copy the contents of `SKILL.md`
2. Add it to your Claude skills directory:
   - Claude Code: place in your project's `.claude/skills/` folder
   - Claude Desktop: follow your platform's skill installation guide

---

## How to Use

### Clone a Writing Style (Mode A)

```
"Analyze my writing style and write a Threads post about [topic]"
"Clone this writing style: [paste sample]"
"Write in my style"
```

Then paste your writing sample when prompted. StyleWriter will:
1. Extract your Style DNA
2. Show you a structured breakdown
3. Generate content in your style
4. Validate the match with a comparison table

### Use a Preset Style (Mode B)

```
"Use the Minimal Storyteller style to write about [topic]"
"Write a LinkedIn article about [topic] in Direct Authority style"
"Use the Conversational Expert preset for a Threads post"
```

---

## Style DNA — What Gets Analyzed

StyleWriter breaks down writing across 7 dimensions:

1. **Sentence Structure** — avg length, short/long ratio, complexity
2. **Rhythm & Flow** — pacing patterns, rhetorical beats
3. **Punctuation Profile** — frequency of commas, dashes, ellipses, colons
4. **Vocabulary Complexity** — simple vs advanced, jargon, colloquialisms
5. **Paragraph Structure** — density, avg sentences per paragraph
6. **Tone & Voice** — formal/conversational/analytical/narrative, POV
7. **Signature Markers** — recurring phrases, what the writer never does

---

## Platform Support

| Platform | Output Format |
|---|---|
| Threads | 1–5 short paragraphs, max 500 chars/post |
| LinkedIn Article | 600–1200 words, structured |
| Blog Post | 800–2000 words, SEO-aware |
| Generic Social | 100–250 words |

---

## Adding Custom Presets

Fork this repo and add your own presets to `SKILL.md` using this format:

```markdown
### PRESET: [Your Preset Name]
*Best for: [platforms]*
- [Style rule 1]
- [Style rule 2]
- Avoids: [what this style never does]
```

To build a preset from a real writing sample: run Mode A → Step 3 (Style DNA card) → convert to preset format.

Pull requests welcome.

---

## Example Output

**Input sample:** A conversational Threads post about productivity (250 words)

**Style DNA extracted:**
- Avg sentence length: 9 words
- Short/long ratio: 3:1
- Punctuation: heavy period use, rare commas
- Tone: conversational, first person, no hedging
- Signature: starts paragraphs with short declarative sentences

**Generated output:** New Threads post on a different topic — matching the same rhythm, pacing, and voice.

**Style Match Accuracy: 91%**

---

## License

MIT — free to use, fork, and adapt.

---

*Built as a Claude skill. Inspired by writing style forensic analysis.*