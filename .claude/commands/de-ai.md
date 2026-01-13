# De-AI-ify Text

Remove AI-generated patterns and restore natural human voice to writing.

## Input

$ARGUMENTS

Provide either:
- A file path to process
- Text directly to clean up

## What Gets Removed

### Overused Transitions
- "Moreover," "Furthermore," "Additionally," "Nevertheless"
- Excessive "However" at sentence starts
- "While X, Y" openings
- "That said," "That being said,"

### AI Clichés
- "In today's fast-paced world"
- "Let's dive deep"
- "Unlock your potential"
- "Harness the power of"
- "At its core"
- "It's important to note"
- "It's worth mentioning"

### Hedging Language
- "I think" when stating facts
- Vague quantifiers: "various," "numerous," "myriad," "a number of"
- "Essentially," "Basically," "Fundamentally,"
- "In order to" (just use "to")

### Corporate Buzzwords
- "utilize" → "use"
- "facilitate" → "help"
- "optimize" → "improve"
- "leverage" → "use"
- "implement" → "do" or "build"
- "synergy" → [delete entirely]

### Robotic Patterns
- Rhetorical questions followed by immediate answers
- Obsessive parallel structure (always three items)
- Announcing what you're about to say
- Summarizing what you just said
- Excessive enthusiasm (!!!)

## What Gets Added

### Natural Voice
- Varied sentence lengths
- Conversational contractions
- Direct statements without hedging
- Specific examples instead of generalities

### Human Rhythm
- Natural transitions (or no transition needed)
- Confident assertions
- Occasional incomplete thoughts
- Real opinions

## Process

1. **Read the original text**
2. **Identify AI patterns**
3. **Rewrite with human voice**
4. **Provide before/after comparison**

## Example

**Before (AI):**
"In today's rapidly evolving digital landscape, it's crucial to understand that leveraging AI effectively isn't just about utilizing cutting-edge technology—it's about harnessing its transformative potential to unlock unprecedented opportunities."

**After (Human):**
"AI works best when you use it for specific tasks. Focus on what it actually does well."

## Output

Provide:
- The cleaned-up text
- A brief summary of changes made
- Any places that need human review (specific examples, personal details, etc.)
