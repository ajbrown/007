# 📡 Project 007 Publishing Guide

```
 ___  _   _ ___  _     ___ ____  _   _ ___ _   _  ____
| _ \| | | | _ )| |   |_ _/ ___|| | | |_ _| \ | |/ ___|
|  _/| |_| | _ \| |    | |\___ \| |_| || ||  \| | |  _
| |  |  _  | |_)| |___ | | ___) |  _  || || |\  | |_| |
|_|  |_| |_|___/|_____|___|____/|_| |_|___|_| \_|\____|
```

This guide covers multiple distribution methods for Project 007 plugin.

## 🎯 Distribution Methods

### Method 1: Direct GitHub Installation (Recommended)

Once pushed to GitHub, users can install directly:

```bash
# Users install with:
claude plugin install ajbrown/007
```

**Requirements:**
1. Push plugin to GitHub repository
2. Ensure `.claude-plugin/plugin.json` is present
3. Tag releases (optional but recommended)

**Setup:**
```bash
# Commit plugin structure
git add .
git commit -m "feat: Project 007 Claude Code plugin v1.0.0"

# Tag the release
git tag v1.0.0
git push origin main --tags
```

**Advantages:**
✓ Simplest for users
✓ Automatic version control
✓ Built-in update mechanism
✓ No marketplace configuration needed

---

### Method 2: Create Your Own Marketplace

Host a custom marketplace for multiple plugins:

#### Step 1: Create Marketplace Structure

```bash
mkdir -p 007-marketplace/.claude-plugin
mkdir -p 007-marketplace/plugins/
```

#### Step 2: Move Plugin to Marketplace

```bash
# Copy Project 007 to marketplace
cp -r 007 007-marketplace/plugins/project-007
```

#### Step 3: Create Marketplace Manifest

**File: `007-marketplace/.claude-plugin/marketplace.json`**
```json
{
  "name": "project-007-marketplace",
  "owner": {
    "name": "AJ Brown",
    "email": "yesreply@happy.engineering"
  },
  "metadata": {
    "description": "Elite agentic workflows and advanced multi-agent orchestration tools",
    "version": "1.0.0",
    "pluginRoot": "./plugins"
  },
  "plugins": [
    {
      "name": "project-007",
      "source": "./plugins/project-007",
      "description": "Elite agentic software delivery workflows - advanced multi-agent orchestration, strategic planning, and autonomous task execution",
      "version": "1.0.0",
      "author": {
        "name": "AJ Brown",
        "email": "yesreply@happy.engineering",
        "url": "https://github.com/ajbrown"
      },
      "homepage": "https://github.com/ajbrown/007",
      "repository": "https://github.com/ajbrown/007",
      "license": "MIT",
      "keywords": [
        "agents",
        "workflows",
        "automation",
        "software-delivery",
        "multi-agent"
      ],
      "category": "productivity"
    }
  ]
}
```

#### Step 4: Host on GitHub

```bash
cd 007-marketplace
git init
git add .
git commit -m "Initial marketplace for Project 007"
git remote add origin https://github.com/ajbrown/007-marketplace.git
git push -u origin main
```

#### User Installation:
```bash
# Add marketplace
claude plugin marketplace add ajbrown/007-marketplace

# Install plugin
claude plugin install project-007@project-007-marketplace
```

**Advantages:**
✓ Can bundle multiple plugins
✓ Centralized plugin catalog
✓ Custom branding
✓ Version control per plugin

---

### Method 3: Submit to Official Anthropic Marketplace

Get Project 007 featured in the official Claude Code plugin directory.

#### Requirements:
- High code quality
- Comprehensive documentation
- Security best practices
- Unique value proposition

#### Submission Process:

1. **Prepare Plugin**
   - Ensure all tests pass
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
   claude plugin install project-007@claude-plugin-directory
   ```

**Advantages:**
✓ Maximum visibility
✓ Anthropic's endorsement
✓ Discoverability via `/plugin > Discover`
✓ Trust and credibility

---

### Method 4: Community Marketplaces

Submit to community-driven marketplaces:

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
✓ Multiple distribution channels
✓ Community exposure
✓ Faster approval than official marketplace
✓ Niche audience targeting

---

## 🔐 Private Distribution

For team or enterprise use:

### Option A: Private GitHub Repository

```bash
# Set GitHub token
export GITHUB_TOKEN=ghp_xxxxxxxxxxxxxxxxxxxx

# Users install with:
claude plugin install ajbrown/007-private
```

### Option B: Internal Marketplace

**Team settings (`.claude/settings.json`):**
```json
{
  "extraKnownMarketplaces": {
    "company-tools": {
      "source": {
        "source": "github",
        "repo": "your-org/claude-plugins"
      }
    }
  },
  "enabledPlugins": {
    "project-007@company-tools": true
  }
}
```

**Advantages:**
✓ Access control
✓ Internal tools integration
✓ Company policy compliance
✓ Customization for team needs

---

## 📦 Version Management

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

### Update manifest:
```json
{
  "version": "1.1.0"
}
```

---

## 🧪 Testing Before Publishing

### Local Testing

```bash
# Install from local directory
cd /path/to/007
claude plugin install .

# Test all commands
claude
> /next-priority
> /write-implementation-plan
> /testing/fix-tests

# Test agents via Task tool
```

### Validation

```bash
# Validate plugin structure
claude plugin validate .

# Check JSON syntax
cat .claude-plugin/plugin.json | jq .
```

---

## 📊 Publishing Checklist

Before publishing, ensure:

- [ ] `plugin.json` has correct version
- [ ] All agents have proper frontmatter with `description` and `capabilities`
- [ ] All commands are tested and working
- [ ] README.md has installation instructions
- [ ] LICENSE file is present
- [ ] PLUGIN.md technical documentation is complete
- [ ] Repository has descriptive README
- [ ] Git tags match plugin version
- [ ] All links in documentation work
- [ ] Security review completed
- [ ] No secrets or credentials in code

---

## 🚀 Recommended Publishing Strategy

For Project 007, we recommend a **multi-channel approach**:

1. **Immediate:** GitHub direct installation (easiest for users)
2. **Short-term:** Submit to 2-3 community marketplaces
3. **Long-term:** Apply to official Anthropic marketplace

This maximizes reach while maintaining flexibility.

---

## 📈 Post-Publishing

### Monitor Usage
- Watch GitHub stars and forks
- Track issues and feature requests
- Monitor community feedback

### Maintain Plugin
- Regular updates for new Claude Code features
- Bug fixes and improvements
- Documentation updates
- Security patches

### Promote Plugin
- Blog post or tutorial
- Social media announcement
- Community forum posts
- Example projects and demos

---

## 🆘 Support

**Issues:** https://github.com/ajbrown/007/issues
**Discussions:** https://github.com/ajbrown/007/discussions
**Documentation:** See PLUGIN.md and README.md

---

```
"Good luck, Agent. The mission is in your hands."
```

*Publishing guide last updated: 2026-01-16*
