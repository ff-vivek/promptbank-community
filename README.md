# PromptBank Community

A community-driven collection of prompts for Claude AI, compatible with [promptbank](https://github.com/ff-vivek/promptbank) CLI.

## Browse Prompts

| Name | Category | Description |
|------|----------|-------------|
| [code-reviewer](prompts/role/code-reviewer.json) | role | Expert code reviewer for thorough PR reviews |
| [technical-writer](prompts/role/technical-writer.json) | role | Technical documentation specialist |
| [debugging-assistant](prompts/skill/debugging-assistant.json) | skill | Systematic debugging and troubleshooting |
| [api-designer](prompts/agent/api-designer.json) | agent | REST API design expert |

## Installation

Install prompts using the promptbank CLI:

```bash
# Install the CLI
cargo install promptbank

# Browse available prompts
promptbank community browse

# Install a prompt
promptbank community install code-reviewer

# Search prompts
promptbank community search "api"
```

## Contributing

We welcome contributions! Here's how to add your prompt:

### 1. Fork this repository

### 2. Create your prompt file

Create a JSON file in the appropriate category folder:

```
prompts/
├── system/     # System prompts
├── skill/      # Specific skills
├── agent/      # Agent personas
├── role/       # Professional roles
├── task/       # Task-specific
└── template/   # Templates with variables
```

### 3. Prompt file format

```json
{
  "name": "your-prompt-name",
  "category": "role",
  "description": "Brief description (under 80 chars)",
  "content": "Your prompt content here...",
  "tags": ["tag1", "tag2"],
  "variables": ["var1", "var2"],
  "author": "your-github-username",
  "version": "1.0.0"
}
```

### 4. Add to index.json

Add an entry to `index.json`:

```json
{
  "name": "your-prompt-name",
  "category": "role",
  "description": "Brief description",
  "author": "your-github-username",
  "path": "prompts/role/your-prompt-name.json",
  "tags": ["tag1", "tag2"],
  "downloads": 0
}
```

### 5. Submit a Pull Request

- Use a descriptive PR title
- Include example usage in the description
- Ensure your prompt is tested and working

## Guidelines

- **Be original**: Don't copy prompts from others without attribution
- **Be clear**: Write prompts that are easy to understand
- **Be specific**: Focused prompts work better than generic ones
- **Test it**: Make sure your prompt works well with Claude
- **No harmful content**: Prompts must follow Anthropic's usage policies

## License

MIT - All prompts are freely available for use.
