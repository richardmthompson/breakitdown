# Installation Guide

## Claude Code (Primary Support)

### Quick Install
1. Download [`breakitdown.md`](../commands/breakitdown.md)
2. Copy to your commands directory:
   ```bash
   cp breakitdown.md ~/.claude/commands/
   ```
3. Use `/breakitdown` in any conversation

### Verify Installation
```bash
ls ~/.claude/commands/breakitdown.md
```

If the file exists, you're ready to go!

## Other AI Assistants

The `/breakitdown` pattern can be adapted to any AI assistant that supports structured task tracking.

### Core Pattern
```
1. Detect complex response (multiple questions/sections)
2. Create sequential checkpoints
3. Present first checkpoint only
4. Wait for user response
5. Mark complete, move to next
6. Repeat until done
```

### GitHub Copilot Chat
**Status:** Adaptation in progress

**Concept:** Use structured prompts with checkpointing:
```
"Break this analysis into sequential steps.
Present one step at a time. Wait for my response before continuing."
```

### Cursor AI
**Status:** Adaptation possible

**Approach:** Similar to Copilot - use explicit checkpointing instructions in custom commands.

### ChatGPT Custom Instructions
**Status:** Partially supported

**Method:** Add to custom instructions:
```
When providing complex analyses or multiple questions:
1. Break into numbered checkpoints
2. Present one checkpoint at a time
3. Wait for my response before proceeding
4. Explicitly ask: "Should I continue to the next checkpoint?"
```

**Limitation:** No native TodoWrite equivalent, so relies on numbered lists and manual progression.

## Contributing Adapters

Have you adapted `/breakitdown` for another AI assistant? **We'd love to include it!**

### What We Need
1. Installation instructions for that platform
2. Example usage
3. Any limitations or differences from Claude Code version
4. Your preferred attribution

Submit via PR or open an issue with your adapter.

## Troubleshooting

### Claude Code: Command Not Recognized
**Problem:** `/breakitdown` returns "unknown command"

**Solutions:**
1. Verify file location: `~/.claude/commands/breakitdown.md`
2. Check file permissions: `chmod 644 ~/.claude/commands/breakitdown.md`
3. Restart Claude Code
4. Try using full path: `cat ~/.claude/commands/breakitdown.md` to verify content

### Command Runs But Doesn't Work As Expected
**Problem:** Command executes but doesn't create proper chunking

**Likely Cause:** AI context may be too full

**Solutions:**
1. Use `/breakitdown` early in conversation
2. Try in a fresh conversation
3. Be explicit: "Use the break it down command to chunk this response"

### Other Issues
Open an issue on GitHub with:
- AI assistant version
- Example of what happened vs. what you expected
- Your use case

We'll help troubleshoot!

## System Requirements

### Claude Code
- Claude Code version: Latest
- No additional dependencies

### Other Assistants
- Varies by platform
- Generally: Any AI with custom command/instruction support

## Updates

Check the repo periodically for:
- New adapter instructions
- Improved chunking strategies
- Bug fixes

Star the repo to get notified of major updates!

---

**Need help?** Open an issue or reach out on [X/Twitter](https://x.com/richardmthompsn)
