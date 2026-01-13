# Claude Code Skills & Commands

A collection of productivity-focused skills and commands for [Claude Code](https://claude.ai/code), demonstrating session continuity, workflow automation, and AI-assisted personal knowledge management.

## Overview

This repository showcases practical patterns for extending Claude Code beyond one-off conversations. The centerpiece is a **session continuity system** (`/handoff` and `/pickup`) that preserves full context across sessions, plus a suite of commands for common workflows like git operations, research, and daily planning.

## What's Included

### 🎯 Skills (Advanced Features)

**Session Continuity:**
- **`/handoff`** - Save session state with automatic timestamps, git checks, and remote backup
- **`/pickup`** - Restore previous session context from handoff files

These skills solve a fundamental problem: AI conversations lose context when you close your terminal. With handoff/pickup, you can pause work on Friday and resume Monday with full context preserved.

### 📝 Commands (Workflow Automation)

**Development:**
- **`/commit`** - Stage, commit, and push changes with generated commit messages

**Writing & Research:**
- **`/de-ai`** - Remove AI-generated jargon and restore human voice to text
- **`/research [topic]`** - Deep research with vault search and synthesis
- **`/thinking [topic]`** - Collaborative thinking partner mode (questions before answers)

**Daily Rhythm:**
- **`/morning`** - Start the day with Prime → Align → Organize framework
- **`/shutdown`** - End-of-day reflection and tomorrow setup
- **`/journal [entry]`** - Quick capture to personal journal
- **`/weekly-review`** - Weekly reflection using Remind → Reflect → Plan

## Quick Start

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/claude-code-skills-demo.git
cd claude-code-skills-demo
```

2. Copy the `.claude` directory to your project:
```bash
# For project-specific installation
cp -r .claude /path/to/your/project/

# For global installation (all Claude Code sessions)
cp -r .claude ~/.claude/
```

3. Restart your Claude Code session to load the new skills and commands

### Configuration

Many commands reference file paths for personal knowledge management. You'll need to customize these paths for your setup:

**Edit these files to match your structure:**
- `.claude/commands/morning.md` - Update file paths for daily planning
- `.claude/commands/shutdown.md` - Update file paths for reflection
- `.claude/commands/journal.md` - Update path to your journal file
- `.claude/commands/weekly-review.md` - Update paths for review files
- `.claude/commands/research.md` - Update vault/resources paths
- `.claude/skills/handoff/SKILL.md` - Customize handoff file location (default: `contexts/_LifeOS/handoff/`)

**Or use as-is** for the development commands:
- `/commit`, `/de-ai`, `/thinking` work without configuration

## Usage Examples

### Session Continuity (The Star Feature!)

```bash
# End of work session - save everything
/handoff

# Next day, or after switching machines
/pickup

# Claude now has full context of what you were working on!
```

**What gets preserved:**
- Session summary and timeline
- Key decisions made
- Code changes committed
- Open questions and blockers
- Next steps and priorities

### Development Workflow

```bash
# Make some changes to your code...

# One command to stage, commit, and push
/commit

# Claude reviews changes, generates appropriate commit message, and pushes
```

### Research & Writing

```bash
# Deep dive on a topic
/research prompt engineering best practices

# Remove AI jargon from your writing
/de-ai path/to/draft.md

# Thinking partner for complex decisions
/thinking should I refactor this module or rewrite it
```

### Daily Rhythm

```bash
# Morning planning (integrates with Things 3, Google Calendar if configured)
/morning feeling scattered, lots on my mind

# End of day reflection
/shutdown completed major refactor, feeling good

# Quick journal capture
/journal had a breakthrough on the architecture today
```

## Demo: Session Continuity System

The handoff/pickup system is production-tested for maintaining context across:
- Multi-day interruptions (family emergencies, weekends)
- Machine switches (laptop to desktop)
- Context window management (compress old sessions, preserve key insights)

**Technical Details:**
- Handoff files use structured markdown with metadata
- Automatic git commit and push for backup
- Date-based file naming for easy lookup
- Supports multiple sessions per day with timestamps
- Pickup can load by date or default to most recent

## Architecture & Design Patterns

### Session State Management

The handoff skill demonstrates:
- **Structured context preservation** - Organized sections for different info types
- **Automatic timestamps** - Uses `date` command for accuracy
- **Git integration** - Checks for uncommitted changes before handoff
- **Remote backup** - Automatic push ensures availability across machines

### MCP Integration

Several commands showcase Model Context Protocol integration:
- Things 3 integration (`/morning` checks tasks)
- Google Calendar integration (`/morning` shows events)
- Granola meeting notes access (research workflows)

### Prompt Engineering Patterns

Commands demonstrate effective prompt patterns:
- **Context injection** via `$ARGUMENTS`
- **Structured output** with markdown templates
- **Conditional logic** (if input provided vs. not)
- **Thinking partner mode** (questions before solutions)

## Real-World Use Cases

**Engineering Leadership:**
- Handoff/pickup for managing interrupted work (meetings, context switches)
- Weekly reviews to track team progress and identify patterns
- Research command for technical deep dives

**Job Search:**
- Morning/shutdown for daily accountability
- Research for company/role investigation
- Thinking partner for career decisions

**Personal Knowledge Management:**
- Journal for daily reflections
- Research for synthesizing learnings
- Weekly reviews for pattern recognition

## Technical Requirements

- [Claude Code CLI](https://claude.ai/code) installed and configured
- Git (for handoff/pickup and commit commands)
- Optional: MCP servers for Things 3, Google Calendar integration

## Customization

These skills and commands are designed as **templates** - fork and customize:

1. **Adapt file paths** to match your directory structure
2. **Modify templates** to match your workflows
3. **Add new commands** - any `.md` file in `.claude/commands/` becomes a command
4. **Extend skills** - create new skills in `.claude/skills/[skill-name]/SKILL.md`

## Background & Motivation

I built this while managing engineering teams at petabyte scale (Marco Polo) and realized Claude Code sessions were too ephemeral for real work. Losing context between sessions meant:
- Re-explaining project context daily
- Forgetting what I was working on
- No continuity across multi-day projects

The handoff/pickup system solved this by treating AI sessions like Git commits - discrete, resumable units of work.

## Production AI Experience

This repo grew out of practical experience:
- **14M+ minutes/month** of ML transcription in production (Whisper STT)
- **Cost optimization** from $1M/month to $20K/month through architecture decisions
- **AWS Inferentia** pioneering work for model optimization
- **MCP orchestration** across Gmail, Calendar, Things 3, Linear, Granola

The skills here apply similar production thinking to personal productivity.

## Contributing

This is a personal workflow repo shared for demonstration, but improvements welcome:
- Bug fixes for edge cases
- Generalization for broader use cases
- New command/skill ideas
- Documentation improvements

## License

MIT License - use, modify, share freely.

## Related Projects

- [Claude Code](https://claude.ai/code) - The CLI tool these skills extend
- [Model Context Protocol](https://modelcontextprotocol.io/) - Framework for AI tool integration
- [PARA Method](https://fortelabs.com/blog/para/) - Organizational framework referenced in commands

## Author

Built by an engineering leader focused on making AI genuinely useful in daily workflows, not just impressive in demos.

Currently exploring AI agent orchestration, production ML infrastructure, and the intersection of personal knowledge management with AI.

---

**Status:** Production-tested in daily use since January 2025. The handoff/pickup system has handled multi-day interruptions, machine switches, and 7+ sessions per day without losing context.
