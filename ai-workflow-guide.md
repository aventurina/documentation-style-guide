# AI-assisted development: a practical workflow

A guide to using AI tools like Claude and ChatGPT throughout a project, not just for autocomplete. This is the workflow I actually use, written up so it's useful to anyone else figuring out where AI genuinely helps and where it needs a closer look.

The short version: AI is fast at producing a first draft of almost anything, a plan, a scaffold, a README. It is not reliably good at knowing when it's wrong. That gap is where you come in, at every step.

## Step 1: Plan before you build

Before writing any code, talk through the idea, the tech stack, and the general approach with an AI tool, and ask it to put together a plan.

If you have access to more than one tool, ask both. Two independent plans give you something to compare instead of a single answer you have no way to check. Read both, then decide: one might be clearly better, or the right answer might be a combination of the two. Either way, you're the one making that call, not the tool.

**Why this matters:** a plan is cheap to throw away. Code you've already written is not. Catching a bad architectural decision at the planning stage saves far more time than catching it after the app is half built.

## Step 2: Let AI scaffold, then take it over

Once you have a plan you trust, have the AI tool build out the initial structure: the app framework, the boilerplate, the first pass at the pieces that follow a known pattern.

Then take over. Make the changes that reflect what you actually want, not just what the plan described in the abstract. This is the point where your own judgment about the product, the edge cases, and the details that matter should start driving the work.

**Common friction point:** it's tempting to keep asking the AI to make every remaining change instead of taking the wheel yourself. The scaffold is a starting point, not a finished product, and the longer you stay in "ask AI for the next change" mode, the less you understand your own codebase.

## Step 3: Draft documentation with AI, then verify it

When the work is done, AI is genuinely useful for a first pass at documentation, the README, setup instructions, an overview of how something works. If you have more than one tool available, ask each of them to generate documentation independently, then compare the two and use whichever is better, or combine the strongest parts of both.

Then check it. Read the generated documentation against how the thing actually behaves, not against how it was supposed to behave. Fill in what's missing, fix what's wrong, and rewrite it so it sounds like a person wrote it, because a person should have.

**Why this matters:** AI-generated documentation reads well and is often wrong in small, specific ways, a flag that isn't quite named correctly, a step that's missing, an edge case left out. It's confident regardless of whether it's accurate, so confidence is not a signal you can trust on its own.

## Common friction points, and what to do about them

- **It sounds right, so it's easy to stop checking.** Fluent output is not the same as correct output. Verify against the actual code or the actual behavior, not against how plausible the explanation sounds.
- **It can't see what it doesn't know.** AI has no visibility into your team's unwritten conventions, your specific deployment setup, or a decision made in a meeting last week. Anything like that needs to come from you, not from a prompt.
- **Two tools rarely fail in the same place.** If you have access to more than one AI tool, use that. Where they agree, you can move faster. Where they disagree, that's exactly where you should slow down and look closer yourself.
- **It's easy to lose your own voice.** AI-drafted text tends toward a generic, slightly formal tone. Read anything it produces out loud before shipping it. If it doesn't sound like you, rewrite the parts that don't.

## A quick review checklist before you ship anything AI helped produce

- Does it match how the code or system actually behaves, not just how it was supposed to work?
- Is anything missing that a person using this would actually need to know?
- Does it sound like a person wrote it, in a voice you'd recognize as your own?
- If two tools produced different answers, did you look closely at both, or just pick the first one?

## The takeaway

AI is a fast way to get a first draft of almost anything. It is not a substitute for understanding what you shipped. Use it to move faster at every stage, planning, building, documenting, but treat every one of its outputs as a draft that needs your judgment before it's real.
