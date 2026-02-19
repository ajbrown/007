# Project 007 - Plugin Marketplace Architecture

```
 _____  _____  _____
|  _  ||  _  ||___  |
| |_| || |_| |   / /
|  _  ||  _  |  / /
|_| |_||_| |_| /_/

PLUGIN DOCUMENTATION
```

This document provides technical details about the Project 007 plugin marketplace architecture for Claude Code.

## Marketplace Structure

Project 007 is a **plugin marketplace** containing one or more plugins. The marketplace manifest lives at the repo root, and each plugin has its own directory under `plugins/`.

```
007/
├── .claude-plugin/
│   └── marketplace.json           # Marketplace manifest (required)
├── plugins/
│   └── ajentic/                   # "ajentic" plugin
│       ├── .claude-plugin/
│       │   └── plugin.json        # Plugin manifest (required)
│       ├── agents/                # Agent definitions
│       │   ├── code-reviewer.md
│       │   ├── frontend-engineer.md
│       │   ├── linear-scrum-master.md
│       │   ├── product-manager.md
│       │   ├── quality-engineer.md
│       │   └── security-reviewer.md
│       └── commands/              # Command definitions
│           ├── next-priority.md
│           ├── write-implementation-plan.md
│           └── testing/
│               └── fix-tests.md
├── docs/                          # Reference documentation
├── CLAUDE.md                      # Project-specific Claude instructions
├── LICENSE                        # MIT License
├── PLUGIN.md                      # This file
├── PUBLISHING.md                  # Distribution guide
└── README.md                      # User-facing documentation
```

## Marketplace Manifest

The `.claude-plugin/marketplace.json` file defines the marketplace and lists available plugins:

```json
{
  "name": "007",
  "owner": {
    "name": "A.J. Brown",
    "email": "aj@ajbrown.org"
  },
  "metadata": {
    "description": "Project 007 - Elite agentic software delivery workflows...",
    "version": "1.0.0",
    "pluginRoot": "./plugins"
  },
  "plugins": [
    {
      "name": "ajentic",
      "source": "./plugins/ajentic",
      "description": "...",
      "version": "1.0.0",
      "keywords": [...],
      "category": "productivity"
    }
  ]
}
```

### Marketplace Fields
- `name`: Marketplace identifier
- `owner`: Marketplace owner information
- `metadata.description`: Marketplace description
- `metadata.version`: Marketplace manifest version
- `metadata.pluginRoot`: Root directory for plugins
- `plugins`: Array of available plugins with source paths

## Plugin Manifest

Each plugin has its own `.claude-plugin/plugin.json`:

```json
{
  "name": "ajentic",
  "version": "1.0.0",
  "description": "Elite agentic software delivery workflows...",
  "author": { ... },
  "homepage": "https://github.com/ajbrown/007",
  "repository": "https://github.com/ajbrown/007",
  "license": "MIT",
  "keywords": [ ... ],
  "commands": [
    "./commands/next-priority.md",
    "./commands/write-implementation-plan.md",
    "./commands/testing/fix-tests.md"
  ],
  "agents": "./agents/"
}
```

### Required Fields
- `name`: Unique plugin identifier (kebab-case)

### Optional but Recommended
- `version`: Semantic versioning (MAJOR.MINOR.PATCH)
- `description`: Brief explanation of plugin capabilities
- `author`: Author information (name, email, url)
- `homepage`: Documentation URL
- `repository`: Source code URL
- `license`: License identifier
- `keywords`: Discovery and search tags
- `commands`: Array of command file paths (relative to plugin root)
- `agents`: Path to agents directory (relative to plugin root)

## Agent Definitions

Agents are markdown files with frontmatter defining their capabilities:

```markdown
---
description: What this agent does and when to use it
capabilities:
  - Capability 1
  - Capability 2
  - Capability 3
---

# Agent Instructions

Detailed operational instructions for the agent...
```

### Agent Frontmatter Schema
- `description` (required): Brief description and usage guidance
- `capabilities` (optional): Array of specific capabilities

### Current Agents (ajentic plugin)

| Agent | Purpose |
|-------|---------|
| `code-reviewer` | Code quality, security, and maintainability analysis |
| `security-reviewer` | Security assessments and vulnerability detection |
| `frontend-engineer` | UI/UX implementation and React components |
| `product-manager` | Requirements and implementation planning |
| `quality-engineer` | Test development and coverage analysis |
| `linear-scrum-master` | Linear project management synchronization |

## Command Definitions

Commands are markdown files with frontmatter defining arguments and behavior:

```markdown
---
description: What this command does
arguments:
  - name: argument_name
    description: Argument purpose
    default: default_value
    required: false
---

# Command Instructions

Detailed instructions for command execution...
```

### Command Frontmatter Schema
- `description` (required): Brief command description
- `arguments` (optional): Array of command arguments
  - `name`: Argument name
  - `description`: Argument purpose
  - `default`: Default value if not provided
  - `required`: Whether argument is required (boolean)

### Current Commands (ajentic plugin)

| Command | Purpose | Arguments |
|---------|---------|-----------|
| `/next-priority` | Autonomous task execution | `implementation_plan_path`, `concurrent_tasks` |
| `/write-implementation-plan` | Strategic planning | `requirements_path`, `plan_path`, `specs_path` |
| `/testing/fix-tests` | Comprehensive test fixing | None |

## Installation

### For Users

```bash
# Add the 007 marketplace
/plugin marketplace add ajbrown/007

# Install the ajentic plugin
/plugin install ajentic@007

# Verify installation
claude plugin list

# Uninstall
claude plugin uninstall ajentic
```

### For Developers

```bash
# Clone repository
git clone https://github.com/ajbrown/007.git
cd 007

# Test the plugin directly
claude --plugin-dir ./plugins/ajentic

# Validate marketplace structure
claude plugin validate .

# Validate individual plugin
claude plugin validate ./plugins/ajentic
```

## Plugin Caching

Claude Code copies plugins to a cache directory for security:
- Plugins cannot access files outside their directory
- Symlinks within plugin are preserved
- Use `${CLAUDE_PLUGIN_ROOT}` in scripts/hooks for portable paths

## Version Management

Project 007 follows semantic versioning for both the marketplace and individual plugins:

- **MAJOR** (X.0.0): Breaking changes to agent/command interfaces
- **MINOR** (0.X.0): New agents, commands, or backward-compatible features
- **PATCH** (0.0.X): Bug fixes, documentation, non-breaking improvements

### Release Process

1. Update version in the plugin's `.claude-plugin/plugin.json`
2. Update version in `.claude-plugin/marketplace.json` plugins array
3. Update CHANGELOG.md with changes
4. Commit: `git commit -m "chore: bump ajentic to X.Y.Z"`
5. Tag: `git tag vX.Y.Z`
6. Push: `git push && git push --tags`
7. Users update via marketplace

## Extending the Marketplace

### Adding a New Plugin

1. Create `plugins/your-plugin/.claude-plugin/plugin.json`
2. Add agents and commands under the plugin directory
3. Add the plugin entry to `.claude-plugin/marketplace.json`
4. Update documentation

### Adding a New Agent to ajentic

1. Create `plugins/ajentic/agents/your-agent.md`:
```markdown
---
description: Your agent description
capabilities:
  - Capability 1
  - Capability 2
---

# Agent Instructions
...
```

2. Claude Code automatically discovers agents in the `agents/` directory
3. No plugin.json update needed (agents directory is referenced)

### Adding a New Command to ajentic

1. Create `plugins/ajentic/commands/your-command.md`:
```markdown
---
description: Your command description
arguments:
  - name: your_arg
    description: Argument description
    default: default_value
    required: false
---

# Command Instructions
...
```

2. Add to `plugins/ajentic/.claude-plugin/plugin.json`:
```json
{
  "commands": [
    ...existing commands...,
    "./commands/your-command.md"
  ]
}
```

3. Bump version in plugin.json
4. Commit and push

## Testing

### Manual Testing

```bash
# Test plugin directly
claude --plugin-dir ./plugins/ajentic

# Test command
claude
> /your-command arg1 arg2

# Test agent via Task tool
> I need to use the your-agent agent
```

### Validation Checklist

- [ ] `marketplace.json` is valid JSON
- [ ] Plugin `plugin.json` is valid JSON
- [ ] All command paths in manifest exist
- [ ] All agents have proper frontmatter
- [ ] All commands have proper frontmatter
- [ ] LICENSE file exists
- [ ] README.md has installation instructions
- [ ] Versions follow semantic versioning

## Troubleshooting

### Marketplace Not Loading
```bash
# Verify marketplace.json syntax
cat .claude-plugin/marketplace.json | jq .

# Check plugin structure
ls -la plugins/ajentic/.claude-plugin/plugin.json
```

### Plugin Not Loading
```bash
# Check Claude debug output
claude --debug

# Verify plugin.json syntax
cat plugins/ajentic/.claude-plugin/plugin.json | jq .

# Check file paths
ls -la plugins/ajentic/agents/ plugins/ajentic/commands/
```

### Command Not Found
- Ensure command path in plugin.json matches actual file location
- Command files must use `.md` extension
- Paths should be relative to plugin root with `./` prefix

### Agent Not Available
- Verify agent file exists in `plugins/ajentic/agents/` directory
- Check frontmatter has required `description` field
- Agent filenames must use `.md` extension

## Contributing

When contributing to Project 007:

1. Fork the repository
2. Create a feature branch
3. Add/modify agents or commands under `plugins/ajentic/`
4. Update version in the plugin's plugin.json (semantic versioning)
5. Update marketplace.json if adding a new plugin
6. Update README.md and PLUGIN.md as needed
7. Test locally with `claude --plugin-dir ./plugins/ajentic`
8. Submit pull request

## Resources

- [Claude Code Plugin Reference](https://code.claude.com/docs/en/plugins-reference)
- [Project 007 Repository](https://github.com/ajbrown/007)
- [Issue Tracker](https://github.com/ajbrown/007/issues)

---

*Built for the agentic development community*

```
"The name's Code... Claude Code."
```
