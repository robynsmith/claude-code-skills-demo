# Morning Manifesto

Start the day with intention using the Prime, Align, Organize framework.

## Input

$ARGUMENTS

Optional: Any context about how you're feeling or what's on your mind.

## Process

1. **Read Current Context**
   - Open `contexts/_LifeOS/☀️ Daily Planning & Morning Manifesto.md`
   - Review the current quests and recent entries
   - Check `contexts/_LifeOS/✅ Quests.md` for active quests

2. **Check External Systems**
   - Fetch today's tasks from Things 3 (use `get_today`)
   - Fetch today's calendar events from Google Calendar
   - **Flag rolled-over high-priority tasks**: Any tasks that already have the ☀️ emoji rolled over from yesterday
     - These are items that were marked as must-do but didn't get completed
     - Call these out explicitly - they may be avoidance items that need attention
   - Present a summary of what's on the schedule and task list

3. **Mark High-Priority Tasks**
   - Ask user which tasks are high-priority for today (the ones they definitely want to complete)
   - Add the ☀️ emoji to the beginning of those task titles in Things 3 using `update_todo`
   - This helps visually differentiate must-do items from nice-to-do items throughout the day

4. **Create Today's Entry**
   - Add a new dated section for today
   - Follow the Prime → Align → Organize structure

5. **If Input Provided**
   - Incorporate the provided thoughts into the appropriate sections
   - Ask clarifying questions if needed to fill in gaps

6. **If No Input Provided**
   - Create the scaffolding with prompting questions
   - Be a thinking partner to help fill it in

7. **Identify Items Being Avoided**
   - Look at Things 3 tasks, especially:
     - Items with the ☀️ emoji that rolled over (were high-priority yesterday but didn't get done)
     - Items that have been rolling for multiple days
   - Ask: "I notice some tasks have been on your list for a while. Are there any you've been avoiding?"
   - **Pay special attention to rolled-over ☀️ tasks** - these were marked as must-do but got skipped, often a sign of avoidance
   - Common avoidance items: checking email, making calls, difficult decisions, tasks with fear/uncertainty
   - **Connect to the feeling:** "What feeling are you avoiding by not doing this task? Can you feel into that emotion for a moment?"
   - Encourage: Take a few breaths and sit with whatever comes up (fear, overwhelm, dread, etc.)
   - Then prompt: "Which avoided items feel important to tackle today? Let's add them to your plan."
   - This directly connects to the "What am I avoiding feeling?" section in Align - name the avoidance, feel it, then embrace it

## Entry Format

```markdown
# [Day of Week], [Month] [Day] [Year]

### Morning Manifesto

**Prime** - Connect with ourselves
- How are we feeling?
  - [feelings, sensations, state]
- What are we grateful for?
  - [gratitude items]

**Align** - Signal & leverage reminder
- What are our Quests?
  - Quarterly: [if defined]
  - Weekly: [current focus]
- What am I avoiding feeling? Let's embrace it!
  - [emotional avoidance to work through]

**Organize** - Let's get organized to avoid overwhelm
- What quests do we want to work on today?
  - [today's focus areas]
  - Don't forget to embrace intensity!

### Evening Shutdown
[Left blank for later]
```

## Thinking Partner Mode

If the person seems uncertain or scattered:
- Ask what's feeling heavy or unclear
- Help identify what they're avoiding
- Connect today's intentions to larger quests
- Remind them: progress over perfection
