<div align="center">
  <h1>Claude Humanizer</h1>
  <p><strong>Strip algorithmic signatures. Enforce natural voice. Write like a human.</strong></p>
  <p>Engineered by <b>Akash Pattanayak</b></p>
</div>

<br/>

## The Premise
LLMs are statistically programmed to produce text that is grammatically perfect, structurally predictable, and entirely devoid of soul. If your output contains words like *delve*, *testament*, or *intricate tapestry*, you are projecting AI signatures.

**Humanizer** is a Prompt-as-Code execution environment that runs natively within the Claude Code CLI. It systematically audits text against 24 empirically proven AI anti-patterns and rewrites it to sound imperceptibly human.

<br/>

## How It Works
Humanizer doesn't trust the AI to self-correct on the first try. It executes an enforced **Two-Pass Audit Workflow**:

1. **The Draft:** Strips the primary offensive language.
2. **The Audit:** Forces the model to aggressively criticize its own output (*"What makes this obviously AI generated?"*).
3. **The Final Cut:** A secondary revision to scrub lingering structural biases, resulting in mixed sentence pacing, tangible opinions, and deliberate structural imperfections.

<br/>

## Local Setup

Humanizer runs as a standalone Claude Code skill without external dependencies. 

Install it directly into your Claude environment by copying the `SKILL.md` framework into your local skills directory:

```bash
# Provision the local skill environment
mkdir -p ~/.claude/skills/humanizer

# Inject the runtime configuration
cp SKILL.md ~/.claude/skills/humanizer/
```

<br/>

## Execution

Invoke the skill directly through the Claude CLI:

```text
/humanizer

[Paste your AI-generated draft here for processing...]
```

Alternatively, invoke it natively during contextual workflows:

```text
Please run the humanizer protocol on the release notes I just drafted.
```

<br/>

## Anti-Pattern Detection Matrix

The core algorithm audits against 24 specific, data-backed linguistic tells.

### 🚫 The "AI Dictionary" (Banned Lexicon)
* `delve`, `underscore`, `testament`, `showcase`, `fostering`, `intricate tapestry`, `pivotal moment`, `evolving landscape`, `vital role`.
* Overused conditional phrasing ("could potentially possibly be argued").
* Sycophantic conversational filler ("I hope this helps!", "Great question!").

### 🚫 Structural Biases
* **Copula Avoidance:** Swapping natural "is/has" verbs for inflated substitutes like "serves as" or "boasts".
* **The Rule of Three:** The persistent algorithmic habit of artificially grouping nouns and adjectives into trios.
* **Negative Parallelisms:** Predictable sentence pacing ("It's not just X, it's Y").

### � Typographical Tells
* Forced inclusion of emojis in headers.
* Title Case formatting for internal bullet points.
* Excessive em-dash (—) utilization.
* Curly quotes (`“ ”`) instead of standard straight quotes (`" "`).

---
> *"The dangerous part is how confident the suggestions look... If you use it to avoid thinking, it will help you ship bugs faster."*

