# Custom Commands

These are reusable prompts for common workflows. Use them by typing `/command-name` in Claude Code.

**Note:** After adding new commands, restart your Claude Code session for them to be recognized.

---

## Available Commands

### Development & Git

| Command | Purpose |
|---------|---------|
| `/commit` | Stage, commit, and push changes with generated commit message |

### Writing & Research

| Command | Purpose |
|---------|---------|
| `/de-ai [path or text]` | Remove AI-generated jargon and restore human voice |
| `/research [topic]` | Deep research with vault search and synthesis |
| `/thinking [topic]` | Thinking partner mode — questions before answers |

### Daily Rhythm

| Command | Purpose |
|---------|---------|
| `/morning [context]` | Start the day with Prime → Align → Organize framework |
| `/shutdown [summary]` | End-of-day reflection and tomorrow setup |
| `/journal [entry]` | Quick capture to personal journal |

### Weekly

| Command | Purpose |
|---------|---------|
| `/weekly-review [focus]` | Weekly review with Remind → Reflect → Plan framework |

---

## Usage Examples

```bash
# Development
/commit
/de-ai path/to/draft.md

# Research & Thinking
/research Claude Code best practices
/thinking how should I architect this feature

# Daily workflows
/morning feeling productive today
/shutdown wrapped up the API integration
/journal breakthrough on the performance issue

# Weekly
/weekly-review focus on team dynamics
```

---

## Customization Required

⚠️ **Important:** Several commands reference file paths specific to a PARA-based knowledge management structure. You'll need to edit these files to match your setup:

**Commands that need path customization:**
- `morning.md` - Lines 14, 16 (daily planning files)
- `shutdown.md` - Line 20 (daily planning file)
- `journal.md` - Line 17 (journal file)
- `weekly-review.md` - Lines 14-17 (review files)
- `research.md` - Line 34 (resources directory)

**Commands that work as-is:**
- `commit.md` - Works in any git repository
- `de-ai.md` - Works with any text input
- `thinking.md` - Generic thinking partner

### Example Path Replacement

**Before (Jarvis-specific):**
```markdown
Open `contexts/_LifeOS/☀️ Daily Planning & Morning Manifesto.md`
```

**After (your structure):**
```markdown
Open `your-vault-path/daily-planning.md`
```

---

## Creating New Commands

1. Add a new `.md` file to this folder
2. The filename becomes the command name (e.g., `my-command.md` → `/my-command`)
3. Use `$ARGUMENTS` in the file to capture text passed after the command
4. Restart Claude Code session to recognize new commands

### Example Command Template

```markdown
# My Command

Brief description of what this command does.

## Input

$ARGUMENTS

## Process

1. Step one
2. Step two
3. Step three

## Output

Describe what the user gets back.
```

---

## Philosophy

These commands demonstrate different AI interaction patterns:

- **`/commit`** - Automation (AI executes workflow)
- **`/thinking`** - Collaboration (AI asks questions)
- **`/de-ai`** - Transformation (AI processes input)
- **`/morning`** - Structured prompting (AI fills template)
- **`/research`** - Synthesis (AI combines sources)

Adapt these patterns to your own workflows.
