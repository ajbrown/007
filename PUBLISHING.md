# Project 007 Publishing Guide

```
 ___  _   _ ___  _     ___ ____  _   _ ___ _   _  ____
| _ \| | | | _ )| |   |_ _/ ___|| | | |_ _| \ | |/ ___|
|  _/| |_| | _ \| |    | |\___ \| |_| || ||  \| | |  _
| |  |  _  | |_)| |___ | | ___) |  _  || || |\  | |_| |
|_|  |_| |_|___/|_____|___|____/|_| |_|___|_| \_|\____|
```

This guide covers distribution methods for the Project 007 plugin marketplace.

## Architecture Overview

Project 007 is a **plugin marketplace** - a repository that contains one or more plugins. Users add the marketplace first, then install individual plugins from it.

**Installation flow:**
```bash
# 1. Add the marketplace
/plugin marketplace add ajbrown/007

# 2. Install plugins from the marketplace
/plugin install ajentic@007
```

## Distribution Methods

### Method 1: GitHub Marketplace (Recommended)

Push to GitHub and users can add the marketplace directly:

```bash
# Users add with:
/plugin marketplace add ajbrown/007

# Then install plugins:
/plugin install ajentic@007
```

**Requirements:**
1. Push repository to GitHub
2. Ensure `.claude-plugin/marketplace.json` is present at repo root
3. Each plugin has its own `.claude-plugin/plugin.json` under `plugins/`
4. Tag releases (optional but recommended)

**Setup:**
```bash
# Commit marketplace structure
git add .
git commit -m "feat: Project 007 marketplace v1.0.0"

# Tag the release
git tag v1.0.0
git push origin main --tags
```

**Advantages:**
- Simplest for users
- Automatic version control
- Built-in update mechanism
- Multiple plugins in one repository

---

### Method 2: Submit to Official Anthropic Marketplace

Get Project 007 featured in the official Claude Code plugin directory.

#### Requirements:
- High code quality
- Comprehensive documentation
- Security best practices
- Unique value proposition

#### Submission Process:

1. **Prepare Marketplace**
   - Ensure all plugins are well-structured
   - Complete documentation
   - Add examples and use cases
   - Security review

2. **Submit Application**
   - Go to: https://clau.de/plugin-directory-submission
   - Fill out submission form
   - Provide repository URL
   - Describe plugin capabilities

3. **Review Process**
   - Anthropic reviews for quality and security
   - May request changes or improvements
   - Approval timeline varies

4. **User Installation (after approval)**
   ```bash
   claude plugin install ajentic@claude-plugin-directory
   ```

**Advantages:**
- Maximum visibility
- Anthropic's endorsement
- Discoverability via `/plugin > Discover`
- Trust and credibility

---

### Method 3: Community Marketplaces

Submit individual plugins to community-driven marketplaces:

#### Available Community Marketplaces:
- https://claudemarketplaces.com/
- https://claudecodemarketplace.com/
- https://github.com/ananddtyagi/cc-marketplace
- https://github.com/ivan-magda/claude-code-marketplace

#### Process:
Each marketplace has its own submission process. Generally:
1. Fork the marketplace repository
2. Add your plugin entry to their `marketplace.json`
3. Submit pull request
4. Wait for review and approval

**Advantages:**
- Multiple distribution channels
- Community exposure
- Faster approval than official marketplace
- Niche audience targeting

---

## Private Distribution

For team or enterprise use:

### Option A: Private GitHub Repository

```bash
# Set GitHub token
export GITHUB_TOKEN=ghp_xxxxxxxxxxxxxxxxxxxx

# Users add marketplace with:
/plugin marketplace add ajbrown/007-private
/plugin install ajentic@007-private
```

### Option B: Internal Marketplace Configuration

**Team settings (`.claude/settings.json`):**
```json
{
  "extraKnownMarketplaces": {
    "007": {
      "source": {
        "source": "github",
        "repo": "your-org/007"
      }
    }
  },
  "enabledPlugins": {
    "ajentic@007": true
  }
}
```

**Advantages:**
- Access control
- Internal tools integration
- Company policy compliance
- Customization for team needs

---

## Version Management

### Semantic Versioning
Follow semver: `MAJOR.MINOR.PATCH`

```bash
# Bug fixes
git tag v1.0.1

# New features (backward compatible)
git tag v1.1.0

# Breaking changes
git tag v2.0.0

# Push tags
git push --tags
```

### Update manifests:
When releasing, update versions in:
1. `plugins/ajentic/.claude-plugin/plugin.json` - plugin version
2. `.claude-plugin/marketplace.json` - plugin version in plugins array

---

## Testing Before Publishing

### Local Testing

```bash
# Test plugin directly
claude --plugin-dir ./plugins/ajentic

# Test all commands
claude
> /next-priority
> /write-implementation-plan
> /testing/fix-tests

# Test agents via Task tool
```

### Validation

```bash
# Validate marketplace structure
claude plugin validate .

# Validate individual plugin
claude plugin validate ./plugins/ajentic

# Check JSON syntax
cat .claude-plugin/marketplace.json | jq .
cat plugins/ajentic/.claude-plugin/plugin.json | jq .
```

---

## Publishing Checklist

Before publishing, ensure:

- [ ] `marketplace.json` has correct version and plugin entries
- [ ] Each plugin's `plugin.json` has correct version
- [ ] All agents have proper frontmatter with `description` and `capabilities`
- [ ] All commands are tested and working
- [ ] README.md has marketplace installation instructions
- [ ] LICENSE file is present
- [ ] PLUGIN.md technical documentation is complete
- [ ] Repository has descriptive README
- [ ] Git tags match marketplace version
- [ ] All links in documentation work
- [ ] Security review completed
- [ ] No secrets or credentials in code

---

## Recommended Publishing Strategy

For Project 007, we recommend a **multi-channel approach**:

1. **Immediate:** GitHub marketplace (easiest for users)
2. **Short-term:** Submit to 2-3 community marketplaces
3. **Long-term:** Apply to official Anthropic marketplace

This maximizes reach while maintaining flexibility.

---

## Post-Publishing

### Monitor Usage
- Watch GitHub stars and forks
- Track issues and feature requests
- Monitor community feedback

### Maintain Marketplace
- Regular updates for new Claude Code features
- Bug fixes and improvements
- Documentation updates
- Security patches
- Add new plugins as capabilities grow

### Promote
- Blog post or tutorial
- Social media announcement
- Community forum posts
- Example projects and demos

---

## Support

**Issues:** https://github.com/ajbrown/007/issues
**Discussions:** https://github.com/ajbrown/007/discussions
**Documentation:** See PLUGIN.md and README.md

---

```
"Good luck, Agent. The mission is in your hands."
```

*Publishing guide last updated: 2026-02-18*
