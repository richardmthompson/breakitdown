# Break It Down Command

Transform overwhelming AI responses into digestible, sequential conversations using TodoWrite.

## The Problem

When AI responses contain:
- Multiple questions at once
- Complex analyses with several sections
- Many options or recommendations
- Dense information dumps

Humans experience cognitive overload and can't process or respond effectively.

## The Solution

Use TodoWrite to chunk complex responses into sequential, digestible pieces that:
- Ask one question at a time
- Wait for answers before proceeding
- Maintain conversation flow instead of delivering lectures
- Create natural checkpoints for understanding

## Your Task

When this command is invoked (or when you detect you're about to overwhelm the user):

### 1. Stop and Assess

Before delivering your response, ask:
- Am I about to ask multiple questions?
- Am I presenting several analyses or options at once?
- Would this be better as a conversation than a monologue?

### 2. Create TodoWrite Structure

Break your intended response into sequential chunks:

```json
[
  {"content": "[First checkpoint - simple question or confirmation]", "status": "pending", "activeForm": "[Present continuous form]"},
  {"content": "[Second checkpoint - clarification or choice]", "status": "pending", "activeForm": "[Present continuous form]"},
  {"content": "[Third checkpoint - next piece of info]", "status": "pending", "activeForm": "[Present continuous form]"},
  {"content": "[Final checkpoint - recommendation or summary]", "status": "pending", "activeForm": "[Present continuous form]"}
]
```

### 3. Execute Sequentially

- Mark first item as `in_progress`
- Present ONLY that piece
- Wait for user response
- Mark completed and move to next
- Repeat until all checkpoints done

### 4. Chunking Principles

**Good chunks:**
- ✅ Ask one question at a time
- ✅ Present one analysis piece at a time
- ✅ Give one recommendation at a time
- ✅ Create natural stopping points
- ✅ Allow user to digest and respond

**Bad chunks:**
- ❌ "Here are 5 questions..."
- ❌ Dumping entire analysis at once
- ❌ Multiple options without pausing
- ❌ Lengthy explanations without checkpoints

## Real Example

### Before (Overwhelming):
```
Here's my analysis of your day structure:

[Time breakdown table]
[Analysis section 1]
[Analysis section 2]
[Analysis section 3]

Questions:
1. Is context engineering blocking VoxPlan?
2. What's the 0.5hr job search block?
3. Should we adjust the schedule?

Recommendations:
- Consider moving X...
- Maybe combine Y...
- You could also Z...
```

### After (Using TodoWrite):
```json
[
  {"content": "Confirm context engineering blocks VoxPlan release", "status": "in_progress"},
  {"content": "Clarify job search activities (0.5hr block)", "status": "pending"},
  {"content": "Present final day structure recommendation", "status": "pending"},
  {"content": "Break down VoxPlan work block into tasks", "status": "pending"}
]
```

Then: "First checkpoint - I need to confirm: Is the context engineering framework currently blocking the VoxPlan release?"

Wait for answer. Mark completed. Move to next.

## When to Use

Invoke this pattern when:
- User says "break it down" or feels overwhelmed
- You catch yourself asking 3+ questions at once
- Your response has multiple distinct sections
- You're presenting several options or paths
- User needs to make decisions but you're giving too much at once

## Edge Cases

**If user wants the full dump:**
- Some users prefer comprehensive responses
- If they explicitly request "give me everything," respect that
- But offer: "Would you prefer this broken down into steps?"

**If already mid-dump:**
- Acknowledge: "I realize I'm dumping a lot at once"
- Offer: "Should I break this into sequential questions?"
- If yes, create TodoWrite and restart with first chunk

**If chunks are interdependent:**
- Some info must be presented together
- Find the smallest coherent unit
- Explain why it's bundled: "These two pieces go together because..."

## Success Criteria

You've succeeded when:
- User can respond to each chunk before moving on
- Conversation feels natural, not lecture-like
- User isn't paralyzed by too many options
- Progress happens through dialogue, not monologue
- TodoWrite creates clear conversation waypoints

## Remember

**This isn't about dumbing down responses.**
It's about respecting human cognitive limits and creating space for:
- Understanding
- Questions
- Processing
- Decision-making
- Actual conversation

**Principle**: Transform monologues into dialogues through intentional chunking.
