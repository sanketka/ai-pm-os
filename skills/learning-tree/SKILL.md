---
name: learning-tree
description: >
  Break down any concept, topic, or domain into a structured learning tree — from foundational roots to actionable leaves — with one primary resource plus alternates in different formats (video, podcast, article, book) at each level. Use this skill whenever the user wants to learn something new, asks "how do I understand X", "break down X for me", "where do I start with X", "explain X from the ground up", or says they want to deeply understand a topic. Also trigger when the user asks for a learning path, curriculum, or roadmap for any subject — technical, business, creative, or scientific. Always use this skill when the user mentions the "tree" framework or wants to go from roots to leaves on a topic.
---

# Tree Learning Skill

Break any topic into a structured **learning tree** — from deep roots to actionable leaves — with one primary resource plus alternates in different formats at each level.

## The Tree Mental Model

```
🍃 LEAF      — The specific thing you want to understand or do
🌿 BRANCH    — The applied area within the field where the leaf sits
🌳 TRUNK     — The named field or discipline
🌱 ROOTS     — The foundational mental models and first principles
```

Learning works best from the foundation up: the leaf doesn't make sense without the branch, the branch is shaky without the trunk, and the trunk won't hold without roots.

### Rendering order

**Always render in this exact order in the response: 🌱 Roots → 🌳 Trunk → 🌿 Branch → 🍃 Leaf.** Roots come first in the response. Leaf comes last.

This is a *teaching* sequence, not a visual tree diagram. Do not invert the order to make leaves appear at the top "like a real tree." The reader builds understanding by starting with the foundation and climbing toward the specific topic they asked about. The payoff (the leaf) lands at the end because by then they have everything they need to actually understand it.

Do not render the tree as a diagram, navigation menu, or interactive UI with arrows pointing between levels. Render each level as a markdown heading followed by prose and resource bullets, in roots-first order.

---

## Step 1: Clarify the Leaf (only when needed)

Ask one clarifying question only if the topic is genuinely ambiguous about **scope** or **depth**:
- Scope ambiguity: "machine learning" could mean many things — building models, reading papers, or working alongside ML engineers.
- Depth ambiguity: "options trading" could mean the mechanics of how they work, or the strategic side.

For specific leaves like "how does HTTPS work" or "what is a Sankey diagram", skip the question and build the tree directly.

---

## Step 2: Build the Tree

Map the topic to four levels. Each level needs:
- A **named label** (e.g., "Probability theory", not "the math behind it")
- A **substantive explanation** (3–5 sentences) — see "Writing the level explanations" below
- **One primary resource plus 2–3 alternates** (see Step 3)

### Writing the level explanations

The explanation at each level is the *teaching*. The resources are pointers to deeper material, but the prose in the response is what actually conveys understanding. **The user is a busy professional or parent who may never click a link — they should understand the concept from your prose alone.**

**Style: WaitButWhy-inspired explainers.** The goal is to make a smart reader feel "oh, I get it now" — not "I have been informed." Two non-negotiables:

**1. Stupid-simple openings.** Start every level assuming the reader knows nothing about it. The first sentence should be something a 12-year-old could understand. Then build up fast — by sentence three or four you can be conveying real depth, but the on-ramp has to be flat. Don't open with the technical term and then explain it; open with the picture and *then* name it.

> **Bad:** "Cardiac electrophysiology is the study of the electrical signals that drive the heart."
> **Good:** "Your heart is basically a wet electrical circuit. Every beat starts with a tiny electrical pulse..."

**2. Analogies do the heavy lifting.** Every level needs at least one concrete analogy to something the reader already knows. "Think of it like..." is the move. Compare to traffic, kitchens, orchestras, libraries, group chats, thermostats, factories — anything from the physical world the reader has touched. The analogy isn't decoration; it's the explanation. The reader should be able to repeat your analogy to a friend and have *them* get it.

> **Bad:** "Self-attention is a mechanism where every token attends to every other token in the sequence."
> **Good:** "Imagine reading a sentence with twenty highlighters, where each highlighter marks the words most relevant to the one you're currently looking at. That's attention."

**3. Carry one core analogy through the tree, building from the foundation up.** Don't give the reader a fresh, unrelated analogy at every level — that breaks the thread. Pick a central metaphor at roots and *build it forward* through trunk, branch, and leaf: roots establishes the analogy, trunk extends it, branch adds to it, leaf shows it in action. Each level should reuse the *same picture* the previous level introduced, just with more on top of it. By the time the reader reaches the leaf, the whole tree should feel like one connected picture that grew across the four levels.

> **Bad:** Roots = "a giant map of words." Trunk = "a kid learning what dogs are." Branch = "highlighters in a sentence." Leaf = "autocomplete." (Four disconnected metaphors — the reader has to start over each time.)
> **Good:** Roots = "a giant map of words." Trunk = "the map gets *drawn* by trial and error, the way a kid learns patterns from examples." Branch = "the highlighter trick lets words on the map *talk to each other*." Leaf = "the model uses the map plus the highlighters to predict the next word." (One picture that builds across the four levels.)

If the analogy you chose at roots doesn't extend forward through the levels naturally, that's a signal you picked the wrong one. Pick another. The whole tree should feel like a single explanation that builds, not a relay race of unrelated metaphors.

### Length: as short as possible, as long as necessary

There is no word count. A level might land in 3 sentences or 8 — whatever it takes to make the concept click cleanly. The two failure modes to avoid:

- **Padding** — adding sentences to feel thorough. If a sentence doesn't add new understanding, cut it.
- **Compression** — leaving out the analogy or the "why does this matter" because you're trying to be brief. Brief but unclear is worse than slightly longer and clear.

**Test:** Re-read each level and ask "could the reader explain this to a friend now?" If no, you cut too much. If you have sentences that don't help them explain it, you padded.

### Tone

Conversational but professional. The reader is smart, busy, and respects their own time. Write like you're explaining something to a peer over coffee — not lecturing, not slangy. Em-dashes and parentheticals are fine; "yo," "wild," and "basically" once-per-level are fine; emoji-laden enthusiasm is not. No academic hedging ("it could be argued that..."), no consultant-speak ("at the end of the day..."), no LinkedIn voice.

### What every level still must do

1. **Define the concept concretely** — in plain words, with the analogy.
2. **Convey the key insight** — the one thing that makes everything else click.
3. **Connect to the level above** — a short sentence: "And this is what [next level] is built on."

### Cross-level connections are mandatory

The tree only works if the levels visibly build on each other. Each level above roots must include at least one explicit connecting sentence:

- **Trunk → Roots**: "This field is built on [roots concept] because…"
- **Branch → Trunk**: "Within [trunk], this branch focuses specifically on [X] because…"
- **Leaf → Branch**: "[Leaf] is a specific instance of [branch concept], where…"

And the **leaf must close the loop** with a synthesis sentence that names roots, trunk, and branch together. Something like: "So when you measure HRV, you're seeing the autonomic nervous system [roots] modulate cardiac electrical timing [trunk] in a way that wearables [branch] can estimate from your wrist."

If a reader can't trace the chain back from the leaf to the roots after reading your response, the tree failed.

### Level definitions

**🌱 Roots — First Principles**
The foundational mental models, math, or conceptual frameworks everything else is built on. Often from adjacent fields (statistics for ML, psychology for UX, thermodynamics for hardware design). The roots explanation should make a reader *feel* why this foundation is load-bearing.

**🌳 Trunk — The Named Field**
The established discipline the topic belongs to. The thing you'd see on a university course catalog or a textbook spine. Examples: "Statistics," "Microeconomics," "Distributed Systems." The trunk explanation should orient the reader to what the field studies and what its central object is.

**🌿 Branch — The Applied Area**
The specific sub-area within the trunk where the topic lives. This is where specialization starts. Examples: "Bayesian Inference" (within Statistics), "Market Design" (within Microeconomics), "Consensus Protocols" (within Distributed Systems). The branch explanation should explain why this sub-area exists as a distinct thing — what problem or opportunity made it cohere.

**🍃 Leaf — The Target Topic**
The specific concept, skill, or question the user asked about. With roots/trunk/branch in place, explain this with real depth (5–8 sentences is fine here) and tie it back to all three lower levels in a closing synthesis.

The trunk/branch distinction matters: if you find yourself saying the same thing twice, the trunk is too narrow. The trunk is the field; the branch is where in the field.

---

## Step 3: Resource Recommendations

At each level, recommend:
- **One primary resource** — marked ⭐. The single best thing you'd hand someone if they could only have one. This is the spine of the recommendation.
- **2–3 alternates** in different formats — for people who learn visually, prefer audio, or want a second angle. Mix formats deliberately across video, podcast, article, and book so every learning style is served somewhere in the tree.

**Always use web_search before recommending resources** — even for topics you think you know. Training data is often stale, especially for video and podcast content. Verify the resource exists, the URL works, and there isn't a better newer option. The exception is canonical texts you're highly confident in (e.g., CLRS for algorithms, Sipser for theory of computation) — but even for these, search for a clean canonical link (publisher page, author site, or Wikipedia).

### Quality bar

Every recommended resource must clear this bar. If it doesn't, find a better one or drop it.

**Prefer:**
- Primary sources (the author/researcher/practitioner directly)
- Canonical works (the thing experts in the field actually cite)
- Free or freely-accessible resources when quality is comparable
- High-signal independent voices (researchers with track records, practitioners with depth)
- Resources from the last 24 months for fast-moving technical topics (AI/ML, web frameworks, security, fitness science with evolving evidence)

**Avoid:**
- SEO content farms and aggregator sites
- Generic Medium posts without author credentials
- Listicles ("Top 10 Ways to…") and clickbait headlines
- Vendor blog posts unless the vendor *is* the canonical source for that topic
- Outdated tutorials that reference deprecated APIs, old paradigms, or superseded research

**The "would I cite this in a 1:1 with a smart friend?" test:** if you'd be embarrassed to recommend it to a thoughtful colleague, drop it. The user is not looking for *any* resource — they're looking for the *right* resource. A shorter list of high-signal links beats a longer list padded with mediocre ones.

Foundational resources (textbooks, seminal papers, classic talks) are exempt from the recency rule — a 1990s Feynman lecture on QM is still the right call. But "foundational" is a high bar, not an excuse to recommend stale 2018 blog posts on a 2026 topic.

### Linking is mandatory

**Every resource must be a real, clickable markdown link.** A name without a URL is not a recommendation — it's homework for the user. If web_search didn't return a usable link for a resource, either find one or replace the resource with something you can link.

Use this exact markdown link format:
```
[**Resource Name**](https://full-url.com)
```

The bold goes *inside* the link brackets so the title renders bold and clickable.

### Bullet formatting

Render every resource as its own markdown list item using a `-` (dash) at the start of the line. **No indentation** under the primary — alternates are siblings, not children. The ⭐ marks the primary; the icon (📖 ▶️ 🎧 🔗 🎓) marks the format.

Exact format to follow:
```
- ⭐ ▶️ [**Primary Resource Title — Author/Channel**](https://example.com) — One sentence on why this one.
- 🔗 [**Alternate Title — Author**](https://example.com) — What this adds vs. the primary.
- 🎧 [**Podcast Episode — Show**](https://example.com) — What this adds vs. the primary.
- 📖 [**Book Title by Author**](https://example.com) — What this adds vs. the primary.
```

Do **not** indent alternates with spaces. Do **not** combine multiple resources on one line. Each bullet starts at column zero with `- `.

### Format icons

- 📖 book or textbook
- ▶️ video or YouTube
- 🎧 podcast or audio episode
- 🔗 article, blog post, or paper
- 🎓 course (Coursera, edX, university OCW)

### What makes a good primary resource at each level

- **Roots**: rigorous, intuition-building, often visual (animated explainers shine here)
- **Trunk**: canonical, comprehensive (textbooks, full courses)
- **Branch**: applied, opinionated (practitioner books, focused courses)
- **Leaf**: current, specific (papers, talks, deep blog posts)

The "what this adds" line for alternates should explain *why someone would pick this over the primary* — e.g., "shorter and more visual," "deeper on the math," "practitioner perspective," "free alternative." If you can't articulate what an alternate adds, drop it.

The learning sequence IS the tree read in order — roots first, leaf last. No separate sequence section needed.

---

## Step 4: One Honest Warning

End with a single honest note (2–3 sentences) about the most common mistake, misconception, or trap when learning this topic. This is the single highest-leverage thing in the response — make it count.

---

## Tone & Format

- Be concrete and specific — never recommend a category ("read a stats book"), always name the exact resource
- **Every resource is a markdown link.** No bare names. If you can't find a URL, replace the resource.
- Match depth to the user's apparent background (pick up on cues in their phrasing)
- Use the tree emojis (🌱 🌳 🌿 🍃) consistently
- Aim for thorough but scannable — headers and resource lists, not walls of prose
- For very broad topics ("physics," "design"), acknowledge it and either narrow it or pick the most likely leaf

---

## Worked Example

**User asks:** "Help me understand how LLMs actually work — I'm a PM, not an engineer."

---

### 🌱 Roots — Probability and Linear Algebra

Imagine a giant map of every word in English. Words with similar meanings live on the same street — "happy" and "joyful" are neighbors, "couch" and "sofa" share a backyard. Now imagine that instead of a 2D map, this map has thousands of dimensions, so every word has a unique address that captures its full meaning. That's **linear algebra** — the math of representing things as positions in space and moving them around.

The other half is **probability** — the math of being unsure on purpose. Instead of guessing one next word, the model produces a ranked list: "the" (40% likely), "a" (25% likely), "this" (10% likely), and so on for thousands of options. Probability lets the model handle the messiness of language, where there's never just one right answer.

Hold onto the map idea — it's going to come up again. Every layer above is going to reuse it.

- ⭐ ▶️ [**3Blue1Brown — Essence of Linear Algebra**](https://www.3blue1brown.com/topics/linear-algebra) — Visual, intuition-first treatment that builds the geometric understanding most explanations skip.
- 🎓 [**Khan Academy — Statistics and Probability**](https://www.khanacademy.org/math/statistics-probability) — Free alternative if you want structured exercises and a refresher on probability specifically.
- 📖 [**Mathematics for Machine Learning by Deisenroth, Faisal & Ong**](https://mml-book.github.io/) — Free PDF; pick this if you want the rigorous version with proofs.

### 🌳 Trunk — Machine Learning

So who draws the map? Nobody, really. That's the whole idea of machine learning.

Think of how a kid learns what a dog is. You don't hand them a definition — you point at dogs over and over until they get it. They see a Labrador, a Chihuahua, a Great Dane, and somehow extract the pattern: "oh, *this* is dog." Machine learning works the same way. You show the system millions of examples and let it figure out the pattern itself.

In our map analogy: the map starts empty. The system reads a sentence, makes a guess about where each word should go, checks how wrong it was, and nudges the words slightly. Do this a few trillion times across the entire internet, and out pops a map where "happy" and "joyful" really are neighbors — not because anyone put them there, but because they kept showing up in similar contexts. The wild part, discovered over the last decade, is that this approach keeps getting better the more you scale it. Bigger model, more data, more compute. Better map.

LLMs are one specific kind of ML system. They're built on a map that was *learned*, not designed.

- ⭐ 🔗 [**A Visual Introduction to Machine Learning — R2D3**](http://www.r2d3.us/visual-intro-to-machine-learning-part-1/) — Walks through how a model learns from data, with no math, in a way that makes the abstraction click.
- 🎓 [**Andrew Ng — Machine Learning Specialization (Coursera)**](https://www.coursera.org/specializations/machine-learning-introduction) — Pick this if you want a structured course rather than a one-page explainer.
- 🎧 [**The TWIML AI Podcast**](https://twimlai.com/podcast/twimlai/) — Audio option for commutes; practitioner-focused conversations rather than pure pedagogy.

### 🌿 Branch — Transformer Architecture

Here's the problem with just having a map. When you read a sentence, the meaning of any one word depends on all the others. "It" in "the dog chased the cat because it was hungry" — which animal is "it"? The map alone can't tell you. You need a way for words to *talk to each other* and figure out who's referring to whom.

That's the trick transformers introduced in 2017, called **attention**. Imagine reading the sentence with a stack of highlighters, one per word. As you read each word, you mark up the *other* words based on how relevant they are to understanding it. For "it," you'd highlight "dog" bright yellow because that's what "it" refers to. The transformer does this for every word, all at once, in parallel. Sounds small. It wasn't.

Before transformers, language models read text one word at a time, like reading with a finger, and forgot the start of long sentences by the end. Attention let every word look at every other word at the same time — and the same architecture now powers ChatGPT, Claude, image generators, and the AI that figured out how proteins fold. So when people say "GPT" or "LLM," they mean a transformer with a learned word-map plus the highlighter trick on top.

- ⭐ ▶️ [**3Blue1Brown — But what is a GPT? Visual intro to transformers**](https://www.youtube.com/watch?v=wjZofJX0v4M) — The clearest visual explanation of what's happening inside the model when it generates text.
- 🔗 [**The Illustrated Transformer — Jay Alammar**](https://jalammar.github.io/illustrated-transformer/) — The classic written walkthrough; better if you prefer reading and want to revisit specific diagrams.
- ▶️ [**Andrej Karpathy — Let's build GPT from scratch**](https://www.youtube.com/watch?v=kCc8FmEb1nY) — Two-hour code-along; pick this if you want to actually see the architecture implemented.

### 🍃 Leaf — How LLMs Actually Work

Put it all together: an LLM uses the highlighter trick on the learned word-map to do exactly one thing — predict the next word. That's it. You give it some text, it gives you a probability for every possible next word, picks one, adds it to the text, and runs the whole thing again. Writing an essay, answering a question, debugging code — all of it is that single trick repeated thousands of times. Think of it like the world's most sophisticated autocomplete.

Training happens in two phases. **Pre-training** is where the model reads a giant slice of the internet and gets terrifyingly good at guessing what comes next — this is where the word-map gets built. **Post-training** is where humans rate its answers and the model gets nudged toward responses that are helpful, honest, and not harmful. Pre-training builds the raw engine; post-training teaches it manners.

As a PM, three things are worth burning into your brain:

- **Context window** is how much text the model can "see" at once — past that limit, it forgets. Bigger window = more it can keep track of.
- **Hallucinations** happen because the model is *always* guessing, even when it has no idea. It doesn't have a "I don't know" mode. Confidence and accuracy aren't connected. This is a feature of how the math works, not a bug to be patched.
- **Prompting vs. fine-tuning** are different levers. Prompting is cheap and only changes one response. Fine-tuning is expensive but reshapes the model's defaults across every response.

So the full stack: probability and linear algebra build a giant word-map [roots], machine learning is *how* that map gets drawn from examples [trunk], the transformer adds the highlighter trick that lets words talk to each other [branch], and the LLM uses all of it to predict one word at a time, over and over [leaf].

- ⭐ ▶️ [**Andrej Karpathy — Intro to Large Language Models (1-hour talk)**](https://www.youtube.com/watch?v=zjkBMFhNj_g) — The single best PM-accessible overview, by someone who built them at OpenAI and Tesla.
- 🎧 [**Lex Fridman Podcast #416 — Andrej Karpathy**](https://lexfridman.com/andrej-karpathy/) — Long-form conversation that covers the same territory with more meandering depth.
- 🔗 [**Anthropic — Core Views on AI Safety**](https://www.anthropic.com/news/core-views-on-ai-safety) — Practitioner-grade primary source on how frontier models actually behave and are evaluated.

---

**One honest warning:** The biggest trap is treating LLMs like databases or search engines. They're not retrieving facts — they're generating plausible-sounding sequences. A model can be confidently wrong about something it "knows" because confidence and accuracy are decoupled in how these systems work. Internalizing this changes how you scope features and write specs.
