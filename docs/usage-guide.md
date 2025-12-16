# Usage Guide

## When to Use `/breakitdown`

### Perfect Use Cases ✅

#### 1. Multiple Questions at Once
**Trigger:** AI asks 3+ questions simultaneously

**Example:**
```
You: "Review my API design"
AI: "I have questions about authentication, rate limiting, error handling,
     versioning, and caching. Let me ask about each..."
You: "/breakitdown"
AI: "First question: What authentication method are you using?"
```

#### 2. Complex Analysis
**Trigger:** AI provides multi-section analysis

**Example:**
```
You: "Analyze my app's performance"
AI: [About to dump 5 sections: metrics, bottlenecks, architecture,
     database, frontend]
You: "/breakitdown"
AI: "Let's go section by section. First, here's the metrics overview..."
```

#### 3. Planning & Decision-Making
**Trigger:** AI offers many options/recommendations

**Example:**
```
You: "Help me choose a database"
AI: [About to compare 6 databases across 10 criteria]
You: "/breakitdown"
AI: "Let's narrow this down. First: What's your primary use case -
     transactional or analytical?"
```

#### 4. Debugging Multi-Step Issues
**Trigger:** AI about to list many potential causes

**Example:**
```
You: "App crashes on production but not locally"
AI: [About to list 12 potential causes]
You: "/breakitdown"
AI: "Let's debug systematically. First: Can you share the error logs?"
```

#### 5. Code Review
**Trigger:** Reviewing large files or multiple issues

**Example:**
```
You: "Review this 800-line component"
AI: [About to dump comprehensive review]
You: "/breakitdown"
AI: "I'll review in sections. Section 1: State management..."
```

### When NOT to Use ❌

#### 1. Simple Questions
**Don't use for:**
- Single, straightforward questions
- Quick clarifications
- Already-chunked responses

**Example:**
```
You: "What's the syntax for array.map in JavaScript?"
AI: [Gives concise answer]
```
No need for `/breakitdown` - response is already digestible.

#### 2. Emergency/Urgent Issues
**Don't use when:**
- You need fast answers
- Production is down
- Time-critical debugging

**Why:** Breaking down adds interaction overhead. Sometimes you need the full picture immediately.

#### 3. Brainstorming Sessions
**Don't use for:**
- Free-flowing idea generation
- Creative exploration
- When you WANT comprehensive options

**Why:** Chunking can artificially constrain creative thinking.

## How to Invoke

### Method 1: Proactive (Recommended)
Invoke BEFORE AI responds with overwhelming content:

```
You: "Analyze my codebase architecture"
You: "/breakitdown"
AI: [Automatically chunks the response]
```

### Method 2: Reactive
Invoke AFTER AI has already given overwhelming response:

```
AI: [Dumps 5 questions and 8 recommendations]
You: "/breakitdown - let's go through this step by step"
AI: "You're right, that was a lot. Let's start over. First question..."
```

### Method 3: Explicit Instruction
Combine with specific guidance:

```
You: "Help me debug this. Use /breakitdown and prioritize by likelihood"
AI: "Breaking this into prioritized checkpoints. Most likely cause first..."
```

## Advanced Patterns

### Pattern 1: Combine with Context
```
You: "I have 30 minutes. Use /breakitdown to help me fix the auth bug"
AI: "Time-boxed debugging. First checkpoint (5 min): Reproduce the issue..."
```

### Pattern 2: Specify Granularity
```
You: "Review this PR. Use /breakitdown but chunk by file, not by issue type"
AI: "File-by-file review. First file: api/auth.ts..."
```

### Pattern 3: Request Prioritization
```
You: "/breakitdown - prioritize by impact"
AI: "Breaking down by impact. Highest impact first..."
```

### Pattern 4: Set Depth Preference
```
You: "Explain microservices. Use /breakitdown with high-level chunks first"
AI: "Starting high-level. Chunk 1: Core concept..."
```

## Best Practices

### ✅ Do This

1. **Use early in conversation** - Better results with fresh context
2. **Be explicit about priorities** - "prioritize by urgency"
3. **Combine with constraints** - "I have 15 minutes"
4. **Guide the chunking** - "break down by component"
5. **Provide feedback** - "that chunk was too big/small"

### ❌ Avoid This

1. **Don't use for simple questions** - Adds unnecessary overhead
2. **Don't expect perfect chunking** - Guide as needed
3. **Don't abandon mid-flow** - Finish checkpoints or explicitly redirect
4. **Don't use when you need full picture** - Sometimes comprehensive is correct

## Example Workflows

### Workflow 1: Architecture Review

```
You: "Review my app architecture"
You: "/breakitdown by layer"

AI: "Layer 1: Frontend architecture
[Analysis]
Should I continue to Layer 2 (Backend)?"

You: "Yes"

AI: "Layer 2: Backend architecture
[Analysis]
Should I continue to Layer 3 (Database)?"

You: "Skip to deployment"

AI: "Jumping to deployment layer
[Analysis]"
```

### Workflow 2: Learning New Concept

```
You: "Teach me React hooks"
You: "/breakitdown - start with basics"

AI: "Checkpoint 1: What are hooks?
[Explanation]
Ready for Checkpoint 2 (useState)?"

You: "Yes, show me code examples"

AI: "Checkpoint 2: useState with examples
[Code examples]
Ready for useEffect?"
```

### Workflow 3: Debugging

```
You: "Production error: 500 on /api/users"
You: "/breakitdown - systematic debugging"

AI: "Debugging checkpoint 1: Reproduce locally
Can you reproduce the error in development?"

You: "No, production only"

AI: "Checkpoint 2: Check production logs
[Asks for specific log entries]"

You: [Provides logs]

AI: "Checkpoint 3: Found the issue - rate limiting
[Explanation and fix]"
```

## Customization

### Adjusting Chunk Size

If chunks are too large:
```
You: "Smaller chunks please"
AI: [Adjusts granularity]
```

If chunks are too small:
```
You: "Combine these next few steps"
AI: [Larger chunks]
```

### Changing Direction

Mid-flow, you can redirect:
```
AI: "Checkpoint 3: Testing strategy..."
You: "Actually, go back to Checkpoint 1 - I need to reconsider that"
AI: [Returns to previous checkpoint]
```

### Skipping Checkpoints

```
AI: "Checkpoint 2: CSS styling..."
You: "Skip styling, go to deployment"
AI: "Jumping to deployment checkpoint..."
```

## Troubleshooting

### "Still overwhelming"
- Request smaller chunks
- Be more specific about what you need first
- Focus on one aspect: "Just authentication for now"

### "Too slow"
- Use only for truly complex responses
- Skip checkpoints you don't need
- Consider if you actually need comprehensive answer

### "Lost the thread"
- Ask AI to summarize checkpoints completed
- Request a "state of conversation" update
- Start fresh conversation if too tangled

## Tips & Tricks

### Tip 1: Time-Box Checkpoints
```
"Each checkpoint should take <5 minutes to discuss"
```

### Tip 2: Visualize Progress
```
"Show me progress after each checkpoint (e.g., 2/5 complete)"
```

### Tip 3: Batch Related Checkpoints
```
"Group related questions together in each checkpoint"
```

### Tip 4: Set Exit Criteria
```
"Stop when we've identified the root cause"
```

## Getting Help

- **Bug?** Open GitHub issue
- **Question?** Start GitHub discussion
- **Suggestion?** Submit PR or issue
- **Chat?** Reach out on [X/Twitter](https://x.com/richardmthompsn)

---

**Pro tip:** The more you use `/breakitdown`, the better you'll get at recognizing when you need it. Trust your cognitive load - if you feel overwhelmed, invoke it!
