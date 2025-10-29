# Expert-Lead Skill - User Guide

## What This Skill Does

Transforms Claude into a top 1% expert who **guides you through questions** rather than giving direct answers. Forces you to think actively instead of passively consuming information.

**The Problem It Solves:**
- You feel "dumber" after using AI because you just receive answers
- You start conversations unclear and end up somewhere random
- You go down rabbit holes and waste time
- You don't structure your thinking before executing

**The Solution:**
This skill makes Claude ask 2-4 sharp questions to clarify what you ACTUALLY want, then guides you strategically to the answer.

## How to Activate

### Method 1: Explicit Trigger (Recommended)
Just say one of these phrases:
- "guide me"
- "expert guidance"
- "assist me"
- "lead me"
- "you are the expert"
- "be my expert"
- "expert mode"
- "help me think through"
- "walk me through"

**Example:**
```
"Guide me on whether I should refactor this to microservices"
```

### Method 2: Auto-Activation
Claude automatically activates when your request:
- Has "should I", "help me think"
- Is ambiguous or vague
- Has multiple possible approaches
- Needs decision-making or planning
- Could go down rabbit holes

**Example (auto-activates):**
```
"I need to improve my codebase"
```
Claude detects vagueness and asks framing questions.

### When It Bypasses (Direct Answer)
Claude skips framing when:
- Request is crystal clear
- Task is trivial (syntax, lookup, obvious bug fix)
- No strategic thinking needed

**Example (bypasses):**
```
"What's the syntax for async/await in C#?"
```
Claude just answers directly.

## The Flow (What Happens)

### Step 1: Rapid Framing (2-4 Questions)
Claude asks ONLY the essentials:
```
Quick framing:
- What's your input? (what you're working with)
- What output do you want? (understanding, decision, code, plan)
- Should I reference your life-goals or project-context skill?
```

### Step 2: Session Frame (Explicit)
Claude frames the session so you both know what you're doing:
```
"Got it. Here's our session:
- Input: [summarize]
- Output: [desired result]
- Processing: [how I'll guide you]

Let's start..."
```

### Step 3: Expert Questioning
Claude guides you with strategic questions:
- Cuts through complexity (2-3 questions to reach core)
- Challenges flawed assumptions directly (no politeness)
- Applies MoSCoW prioritization
- Prevents rabbit holes

**Intensity auto-adjusts:**
- High: Architecture, major decisions (deep questioning, devil's advocate)
- Medium: General problem-solving (balanced)
- Low: Debugging, small tasks (light guidance)

### Step 4: Smart Checkpoints (Light Touch)
Claude only checkpoints when:
- Detects confusion/contradiction in your responses
- You shift direction unexpectedly
- You're 3+ levels into tangents

```
"⚠️ CHECKPOINT: Started with [X], now on [Y]. Still serving your goal?"
```

### Step 5: Explicit Handoff
When clarity is achieved, Claude asks:
```
"I have enough context. Ready to execute?"
```

Then explicitly states what it will create:
```
"Here's what I'll create:
- Output: [specific deliverable]
- Using: [docx skill / code generation / etc.]
- Based on: [key decisions]

Executing now..."
```

## User Controls (Your Override Commands)

### Skip Framing
When you know what you want and don't need questions:
```
"skip framing, just answer"
```

### More Depth
When you want deeper questioning:
```
"more depth"
```

### Too Many Questions
When you're overwhelmed:
```
"too many questions"
```
Claude reduces to 1-2 essentials only.

### Force Handoff
When you have enough context:
```
"I have enough context, ready to execute?"
```

## Integration with Other Skills

Expert-lead **wraps around** other skills - it guides the planning, then hands off execution.

**Example flow:**
```
You: "Guide me on creating a project proposal"
Claude: [Asks framing questions]
You: [Answers]
Claude: "Should I reference your project-context skill?"
You: "Yes"
Claude: [Loads project context, asks strategic questions]
You: [Clarifies goals]
Claude: "Ready to execute?"
You: "Yes"
Claude: "Executing now using docx skill to create the proposal..."
[Creates document using docx skill]
```

## Mental Models (Your Daily Practice)

These are the two core thinking frameworks built into expert-lead. Master these first.

### 1. Inversion (Charlie Munger) - YOUR DAILY PRACTICE

**What it is:**
Instead of asking "How do I succeed?", ask "How do I guarantee failure?"

**Why it works:**
- Easier to identify failure paths than success paths
- Avoiding stupidity is easier than seeking brilliance
- Reveals hidden risks you'd otherwise miss

**How Claude applies it:**
```
"What would guarantee failure here? Let's avoid those paths."
"What's the worst decision you could make? Now do the opposite."
"If you wanted this to fail spectacularly, what would you do?"
```

**Your practice:**
Use this daily for:
- Investment decisions: "What guarantees I lose money?"
- Code architecture: "What makes this unmaintainable?"
- Life decisions: "What would I definitely regret?"

**Example:**
```
You: "Should I refactor to microservices?"
Claude: "Let's invert: What would make microservices a disaster 
         for your team? Small team, limited devops, tight deadlines, 
         no monitoring. Those guarantee failure. Avoid."
```

### 2. 80/20 Rule (Pareto Principle)

**What it is:**
20% of efforts typically produce 80% of results. Find that 20%.

**Why it works:**
- Most work is noise/busywork
- Forces ruthless prioritization
- Cuts through feature creep and scope bloat

**How Claude applies it:**
```
"Which 20% of this gives 80% of the value?"
"What's the minimum that would work?"
"If you could only do 2 of these 10 things, which ones?"
```

**Your practice:**
Use this to:
- Prioritize features: Which few matter most?
- Cut tasks: What can you eliminate?
- Focus effort: Where's the leverage?

**Example:**
```
You: "I have 15 code improvements to make"
Claude: "Which 2-3 improvements would give you 80% of the benefit? 
         Let's do those first, maybe skip the rest."
```

### How to Use These

**Automatic (Claude applies when relevant):**
```
"Guide me on this decision"
[Claude automatically applies inversion or 80/20 as appropriate]
```

**Explicit request:**
```
"Use inversion to find risks"
"Apply 80/20 to prioritize this"
```

**Daily practice reminder:**
- Morning: "What would make today a failure?" (inversion)
- Planning: "What 20% of tasks matter most?" (80/20)
- Decisions: "What guarantees a bad outcome?" (inversion)

---

**That's it. Two models. Master these before worrying about others.**

## Real-World Examples

### Example 1: Software Development

**You:** "Lead me on this architecture decision"

**Claude:**
```
Quick framing:
- What's the scale and complexity? (team size, load, features)
- What's driving this question? (pain points, concerns, hype?)
- Should I reference your project-context skill?
```

**You:** "3 devs, B2B SaaS, worried about scaling"

**Claude:**
```
Got it. Here's our session:
- Input: Small team, B2B SaaS, scaling concerns
- Output: Architecture decision
- Processing: Challenge assumptions, guide to right-sized architecture

Why microservices? What problem are you actually solving?
```

[Continues questioning, reveals premature optimization, guides to monolith-first]

### Example 2: Learning & Research

**You:** "Expert guidance - I'm reading 5 blog posts about index investing"

**Claude:**
```
Quick framing:
- What's your goal? (understand basics, make decisions, build strategy)
- What output would help? (summary, action plan, investment strategy)
- Should I reference your life-goals skill?
```

**You:** "Yes, check my life-goals. I want to create an investment plan."

**Claude:**
```
Got it. Session frame:
- Input: 5 blog posts on index investing
- Output: Personal investment plan
- Processing: Connect to life-goals, extract principles, build strategy
- Connected: life-goals skill

[Reads your life-goals skill]

I see you have a goal: "Invest €100k in 3 years, 60% index, 40% Bitcoin"

Before we dive in: Where are you NOW on this goal?
```

[Continues with questions in context of your specific goal]

### Example 3: Decision-Making

**You:** "Should I take this job offer?"

**Claude:**
```
Quick framing:
- What's the decision timeframe?
- What's your current situation?
- What does success look like for you 2 years from now?
```

**You:** [Answers]

**Claude:**
```
Got it. Session frame:
- Input: Job offer decision
- Output: Clear recommendation with reasoning
- Processing: Compare options, stress-test assumptions, apply mental models

Let's use inversion (Munger): What would make this job a disaster?
```

[Continues with strategic questions to reveal true priorities]

## Tips for Best Results

### 1. Be Honest in Framing
When Claude asks what you want, be specific:
- ❌ "I want to understand this"
- ✅ "I want to build an investment strategy I can act on this month"

### 2. Don't Rush the Questions
The framing phase feels like overhead, but it saves massive time later. Let Claude ask 2-4 questions - they're cutting through noise.

### 3. Use Override Commands
If Claude is overwhelming you or you know what you want:
- "skip framing"
- "too many questions"
- "I have enough context, ready to execute?"

### 4. Reference Your Other Skills
When relevant, tell Claude to reference:
- Your life-goals skill (long-term goals, progress)
- Your project-context skill (ongoing work)
- Any domain-specific skills

### 5. Give Feedback
If Claude's approach isn't working:
- "more depth" → increases questioning
- "skip framing" (multiple times) → Claude learns to reduce intensity

### 6. Trust the Checkpoints
When Claude says "⚠️ CHECKPOINT", you've probably drifted. Take a moment to refocus.

## What Makes This Different

**Normal Claude:**
```
You: "Help me with my architecture"
Claude: [Gives generic architecture advice]
You: [Passively reads, doesn't think deeply]
```

**Expert-Lead Claude:**
```
You: "Guide me on my architecture"
Claude: "Quick framing: What's your scale, what's driving this, 
         should I reference your project-context?"
You: [Forced to clarify what you actually want]
Claude: "Got it. Let's start: What problem are you solving?"
You: [Active thinking, discovering insights]
Claude: "That assumption won't scale. Try this instead..."
You: [Learning the thinking process]
Claude: "Ready to execute?"
```

**Result:** You walked away smarter, not dumber.

## Feedback Loop

Expert-lead learns from your behavior:
- Say "skip framing" often → It reduces intensity over time
- Say "more questions" → It increases depth
- Interrupt often → It recognizes you're overwhelmed and adjusts
- Engage deeply → It maintains or increases depth

## Troubleshooting

**Problem:** "Claude is asking too many questions"
**Solution:** Say "too many questions" or "skip framing, just answer"

**Problem:** "I don't know what output I want yet"
**Solution:** Say "I'm not sure what I want yet, help me figure it out"

**Problem:** "Claude is being too polite about my bad ideas"
**Solution:** This skill makes Claude direct. If it's not, say "be more direct, challenge my assumptions"

**Problem:** "We went down a rabbit hole"
**Solution:** Wait for the checkpoint, or say "we're off track, let's refocus on [original goal]"

**Problem:** "The framing phase takes too long"
**Solution:** Claude asks max 2-4 questions. If it feels long, your request was very vague. Next time, start with clearer input/output in your initial message.

## Installation

1. Download `expert-lead.skill` file
2. Open Claude desktop
3. Go to Settings → Skills
4. Click "Import Skill"
5. Select `expert-lead.skill`
6. Done!

## Backup & Sharing

The `.skill` file is just a zip file. To backup:
- Store it in GitHub, Dropbox, or anywhere
- Unzip to view/edit contents:
  ```bash
  unzip expert-lead.skill
  ```

## Quick Reference Card

| What You Say | What Happens |
|--------------|--------------|
| "guide me", "expert guidance", "lead me" | Activates expert-lead mode |
| "skip framing, just answer" | Bypasses to direct answer |
| "more depth" | Increases questioning intensity |
| "too many questions" | Reduces to 1-2 questions only |
| "I have enough context, ready to execute?" | Forces handoff to execution |
| Vague request (auto-detected) | Auto-activates expert-lead |
| Clear, trivial request | Bypasses to direct answer |

## Advanced Usage

### Combine with Life-Goals Skill
```
You: "Guide me on my career decision. Reference my life-goals."
Claude: [Reads life-goals, asks questions in context of long-term goals]
```

### Combine with Project-Context Skill
```
You: "Expert guidance on this architecture. Use my project-context."
Claude: [Loads project details, asks relevant questions]
```

### Chain Multiple Sessions
```
Session 1: "Guide me on investment strategy" [Planning]
Session 2: "Using that strategy, guide me on this specific stock" [Decision]
Session 3: "Execute: create investment plan document" [Creation]
```

## Success Metrics

You know this skill is working when:
- ✅ You feel you're thinking more actively
- ✅ Your goals are clear before you start executing
- ✅ You don't go down as many rabbit holes
- ✅ You learn HOW to think about problems, not just get answers
- ✅ You feel guided by an expert, not a generic assistant

## Support

- File issues or improvements by asking Claude to help refine the skill
- Export your version: unzip the .skill file and edit SKILL.md
- Share improvements with others

---

**Remember:** This skill transforms Claude from an answer machine into a thinking partner. Embrace the questions - they're cutting through noise and making you smarter.
