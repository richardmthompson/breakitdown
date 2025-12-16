<div align="center">

<img src="assets/breakitdown-icon.png" alt="Break It Down" width="400"/>

# Break It Down

### Transform Overwhelming AI Responses into Digestible Conversations

Stop drowning in AI responses. Start having conversations.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

</div>

## The Problem

AI assistants are getting better at providing comprehensive answers. But comprehensive ≠ digestible.

When your AI gives you:
- 🤯 5 questions at once
- 📚 Dense multi-section analysis
- 🔀 10 options to evaluate
- 🧠 Complex recommendations requiring decisions

Your brain does this: 😵 **Cognitive overload**

## The Solution

`/breakitdown` transforms monologues into dialogues by chunking complex AI responses into sequential, digestible pieces.

### Before (Overwhelming)
```
AI: "Here are 5 questions about your architecture:
1. Is context engineering blocking VoxPlan?
2. What's your deployment strategy?
3. Should we refactor the auth system?
4. Have you considered microservices?
5. What's your testing coverage?

Also, here's my analysis... [3 more paragraphs]"

You: 😰 (where do I even start?)
```

### After (Using `/breakitdown`)
```
AI: [Creates TodoWrite tracking each question]

"First checkpoint - let's tackle this one at a time:

Is context engineering currently blocking the VoxPlan release?"

You: "Yes, it is."

AI: [Marks completed, moves to next]

"Got it. Second question: What's your deployment strategy?"

You: "Docker on AWS."

AI: [Progress continues naturally...]
```

## Why Your Brain Needs This

**Cognitive Science Foundation:**
- **Working memory capacity**: 4±1 chunks (Cowan, 2001)
- **Cognitive load**: Exceeding capacity impairs decision-making
- **Sequential processing**: Humans excel at focused attention, not parallel information

**The `/breakitdown` Approach:**
- ✅ Respects working memory limits
- ✅ Creates natural conversation flow
- ✅ Builds in checkpoints for understanding
- ✅ Prevents decision paralysis
- ✅ Maintains context without overwhelming

## Installation

### For Claude Code Users

1. **Download the command file:**
   - Copy [`commands/breakitdown.md`](commands/breakitdown.md) from this repo

2. **Add to your commands directory:**
   ```bash
   cp breakitdown.md ~/.claude/commands/
   ```

3. **That's it!** Use `/breakitdown` in any Claude Code conversation.

### For Other AI Assistants

The concept works anywhere with structured task tracking:
- Adapt the TodoWrite pattern to your tool
- Core principle: **chunk → present → wait → repeat**

## Usage

### When to Use `/breakitdown`

Invoke when AI gives you:
- **Multiple questions** (3+) at once
- **Complex analyses** with many sections
- **Many options** to evaluate
- **Dense information** dumps
- **Planning sessions** requiring decisions

### How It Works

1. **AI detects** complexity in its pending response
2. **Creates TodoWrite structure** breaking it into chunks
3. **Presents first chunk** only
4. **Waits** for your response
5. **Marks complete** and moves to next
6. **Repeat** until all checkpoints done

### Real Examples

#### Example 1: Planning a Feature
```
You: "Help me plan the authentication refactor"
AI: [About to dump entire architecture analysis]
You: "/breakitdown"
AI: "Let's break this down step by step:

First - what authentication method are you currently using?"
```

#### Example 2: Debugging Complex Issue
```
You: "The app crashes on startup but only in production"
AI: [About to list 10 potential causes + solutions]
AI (using breakitdown): "Let's investigate systematically:

First - can you share the error logs from production?"
```

#### Example 3: Reviewing Code
```
You: "Review this 500-line file for issues"
AI: [About to dump comprehensive review]
AI (using breakitdown): "I'll review this in sections:

Section 1: Error handling patterns
[analysis]

Should I continue to Section 2 (state management)?"
```

See [`examples/`](examples/) for detailed before/after comparisons.

## The Science: Why This Works

As a cognitive scientist turned AI engineer, I built this on established research:

### Working Memory Limits
- **Baddeley & Hitch (1974)**: Working memory is limited
- **Cowan (2001)**: ~4 chunks maximum capacity
- **When exceeded**: Cognitive overload, poor decisions, information loss

### Sequential vs. Parallel Processing
- Humans excel at **sequential focused attention**
- **Parallel information** overwhelms decision-making systems
- **Conversation > monologue** for complex topics

### Checkpointing & Confirmation
- Breaking problems into checkpoints **improves outcomes**
- Confirmation loops **prevent misunderstanding compounding**
- Natural rhythm **matches how humans think**

Read more in [`docs/cognitive-science-background.md`](docs/cognitive-science-background.md)

## Who This Is For

- **Developers** using AI coding assistants
- **AI Engineers** building with LLMs
- **Product Managers** planning with AI
- **Researchers** working with complex AI outputs
- **Anyone** experiencing AI response overwhelm

## Documentation

- **[Installation Guide](docs/installation.md)** - Detailed setup for different AI assistants
- **[Usage Guide](docs/usage-guide.md)** - Comprehensive examples and patterns
- **[Cognitive Science Background](docs/cognitive-science-background.md)** - The research behind it

## Contributing

Found a bug? Have an improvement? **PRs welcome!**

### Areas for Contribution
- Adapters for other AI assistants (Copilot, Cursor, etc.)
- Additional usage examples
- Improved chunking strategies
- Documentation improvements
- Translations

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Roadmap

- [ ] Adapters for popular AI assistants
- [ ] Visual examples and demo videos
- [ ] Community use case library
- [ ] Integration with other productivity tools
- [ ] Research paper on cognitive benefits

## Credits

**Built by [Richard Thompson](https://x.com/richardmthompsn)**

- Cognitive Scientist → AI Engineer
- 2 years self-taught AI development
- Building voice-first cognitive systems
- Sharing everything I learn

**Background:**
- MSc Cognitive Science (researching working memory & attention)
- Building [Coherence](https://github.com/RichardMizrahi/VoxManifestorApp) - voice-first AI for Android
- Writing about cognitive architecture for AI at [my blog](https://richardmthompson.hashnode.dev/)

## Philosophy

**Old school hacker ethos**: Build useful tools. Give them away.

This tool exists because:
- AI overwhelm is a real problem
- Cognitive science has solutions
- Good tools should be free
- Building in public creates better software

If this helps you, **star the repo** and **share it**. That's how we build better tools together.

## License

MIT License - Use it, modify it, share it.

See [LICENSE](LICENSE) for details.

## Connect

- **X/Twitter**: [@richardmthompsn](https://x.com/richardmthompsn)
- **LinkedIn**: [richardthompsoncognitivescientist](https://linkedin.com/in/richardthompsoncognitivescientist/)
- **Blog**: [richardmthompson.hashnode.dev](https://richardmthompson.hashnode.dev/)

Building in public. One tool at a time.

---

*If this helped you, ⭐ star the repo and share it with others facing AI overwhelm.*
