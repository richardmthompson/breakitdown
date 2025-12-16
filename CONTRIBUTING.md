# Contributing to Break It Down

First off, thank you for considering contributing! This tool exists to help people, and your contributions make it better for everyone.

## How Can I Contribute?

### Reporting Bugs

**Before submitting a bug report:**
- Check existing issues to avoid duplicates
- Gather information about your environment (AI assistant version, OS, etc.)
- Try to reproduce the issue

**When submitting:**
- Use a clear, descriptive title
- Describe the expected vs. actual behavior
- Include steps to reproduce
- Add any relevant screenshots or error messages

### Suggesting Enhancements

We love new ideas! Enhancement suggestions are tracked as GitHub issues.

**When suggesting:**
- Use a clear, descriptive title
- Provide detailed description of the enhancement
- Explain why this would be useful
- Include examples if possible

### Adapters for Other AI Assistants

This is a high-value contribution! If you've adapted `/breakitdown` for another AI assistant:

**Include:**
1. Installation instructions for that platform
2. Usage examples
3. Any limitations vs. Claude Code version
4. Your preferred attribution

**File location:**
- Add to `docs/adapters/[assistant-name].md`
- Update main README with link
- Add to installation.md

### Documentation Improvements

- Fix typos or unclear explanations
- Add more examples
- Improve installation instructions
- Translate to other languages

### Code Contributions

While this is primarily a documentation/command project, code contributions might include:
- Automated testing for command functionality
- Tools to help adapt for other assistants
- Scripts to validate installations

## Pull Request Process

1. **Fork the repo** and create your branch from `main`
2. **Make your changes**
3. **Test thoroughly** - ensure your changes work as expected
4. **Update documentation** - if you've changed functionality
5. **Write clear commit messages**
6. **Submit the PR** with a clear description

### PR Guidelines

**Good PR title examples:**
- "Add Cursor AI adapter documentation"
- "Fix typo in cognitive-science-background.md"
- "Improve installation instructions for Windows"

**In your PR description:**
- What does this change?
- Why is it needed?
- How has it been tested?
- Any breaking changes?

## Code of Conduct

### Our Standards

**Positive behavior:**
- Using welcoming, inclusive language
- Respecting differing viewpoints
- Accepting constructive criticism gracefully
- Focusing on what's best for the community
- Showing empathy towards others

**Unacceptable behavior:**
- Harassment, trolling, or insulting comments
- Personal or political attacks
- Publishing others' private information
- Any conduct inappropriate in a professional setting

### Enforcement

Violations may result in:
1. Warning
2. Temporary ban
3. Permanent ban

Report issues to: [richardthomps1@gmail.com](mailto:richardthomps1@gmail.com)

## Development Setup

### Local Testing (Claude Code)

1. Clone your fork
2. Copy command to your `.claude/commands/` directory
3. Test in Claude Code conversations
4. Verify documentation accuracy

### Documentation Testing

1. Read through your changes
2. Verify all links work
3. Check code examples for accuracy
4. Ensure markdown renders correctly

## Style Guidelines

### Documentation Style

- **Clear and concise** - Respect reader's time
- **Examples over theory** - Show, don't just tell
- **Practical focus** - How does this help users?
- **Conversational tone** - Professional but friendly

### Markdown Conventions

- Use `**bold**` for important terms
- Use `code blocks` for commands and code
- Use headings hierarchically (H2 → H3 → H4)
- Include blank lines between sections

### Example Format

When adding examples:
```markdown
#### Example: [Clear Title]
**Use case:** [When to use this]

**Input:**
```
[What the user types]
```

**Output:**
```
[What happens]
```

**Why it works:** [Brief explanation]
```

## Recognition

Contributors are recognized in:
- README.md (Contributors section - to be added)
- Release notes (for significant contributions)
- Adapter documentation (for adapter authors)

## Questions?

- **GitHub Discussions** - General questions
- **GitHub Issues** - Specific problems
- **X/Twitter** - [@richardmthompsn](https://x.com/richardmthompsn)

---

## Quick Contribution Checklist

- [ ] Issue created (if applicable)
- [ ] Fork created
- [ ] Changes made
- [ ] Changes tested
- [ ] Documentation updated
- [ ] Commit messages clear
- [ ] PR description complete
- [ ] Ready for review!

---

**Thank you for contributing! Every improvement, no matter how small, makes this tool better for everyone.**
