# Installation Guide

Complete installation instructions for the LinkedIn Thought Leadership Skill.

## 📋 Prerequisites

### Required
- **Claude Desktop** (recommended) or **Claude.ai** web access
- **Claude Skills** capability enabled in your account
- Basic familiarity with markdown files

### Recommended
- **Text editor** for editing markdown (VS Code, Sublime Text, Atom, or similar)
- **GitHub account** if you want to fork and customize
- **LinkedIn account** with Creator Mode enabled

### System Requirements
- **OS:** macOS, Windows, or Linux
- **Disk space:** ~5 MB (unpopulated), up to 50 MB (fully populated with your assets)
- **Internet:** Required for Claude access

---

## 🚀 Installation Methods

Choose the method that best fits your workflow:

### Method 1: Direct Download (Easiest)

**Best for:** Most users who want to get started quickly

1. **Download the latest release:**
   - Go to [Releases](https://github.com/ktg0066/LinkedIn-skill/releases)
   - Download `linkedin-thought-leadership-skill-v1.0.0.zip`

2. **Extract the archive:**
   ```bash
   # macOS/Linux
   unzip linkedin-thought-leadership-skill-v1.0.0.zip
   
   # Windows
   Right-click → Extract All
   ```

3. **Add to Claude:**
   - **Claude Desktop:** Settings → Skills → Add Skill → Select the `linkedin-thought-leadership` folder
   - **Claude.ai:** Settings → Capabilities → Skills → Upload the `linkedin-thought-leadership` folder

4. **Verify installation:**
   - Ask Claude: "Do you have the LinkedIn thought leadership skill?"
   - Claude should confirm and describe the skill

### Method 2: Git Clone (For Developers)

**Best for:** Developers who want to contribute or stay updated with git

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ktg0066/LinkedIn-skill.git
   cd LinkedIn-skill
   ```

2. **Add to Claude:**
   - Point Claude to the `linkedin-thought-leadership` folder within the cloned repo

3. **Stay updated:**
   ```bash
   # Pull latest changes
   git pull origin main
   ```

### Method 3: Fork & Customize (For Advanced Users)

**Best for:** Users who want to heavily customize and maintain their own version

1. **Fork the repository** on GitHub
   - Go to https://github.com/ktg0066/LinkedIn-skill
   - Click "Fork" button

2. **Clone your fork:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/LinkedIn-skill.git
   cd LinkedIn-skill
   ```

3. **Customize as needed:**
   - Edit templates
   - Add your own reference materials
   - Modify structures

4. **Add to Claude:**
   - Point Claude to your customized `linkedin-thought-leadership` folder

5. **Keep in sync (optional):**
   ```bash
   # Add upstream remote
   git remote add upstream https://github.com/ktg0066/LinkedIn-skill.git
   
   # Fetch upstream changes
   git fetch upstream
   
   # Merge upstream changes
   git merge upstream/main
   ```

---

## ⚙️ Post-Installation Setup

### Step 1: Verify Installation (2 minutes)

Test that the skill is working:

**Ask Claude:**
```
Do you have access to the LinkedIn thought leadership skill?
```

**Expected response:** Claude should confirm it has the skill and briefly describe its capabilities.

### Step 2: Configure Personalization (15 minutes)

This is **critical** for getting value from the skill!

1. **Open the skill folder** in your text editor

2. **Navigate to:** `SKILL.md`

3. **Find the section:** `🎯 PERSONALIZATION SETTINGS` (near the top)

4. **Fill in your information:**

```markdown
**Name:** [Your full name]
**Current Role:** [Your job title]
**Organization:** [Your company]
**Industry/Domain:** [Your primary industry]

**Core Expertise Areas (3-5 topics):**
1. [Topic 1]
2. [Topic 2]
3. [Topic 3]

**Target Audience:**
- Primary: [Who you're trying to reach]
- Secondary: [Secondary audience]
- Geographic focus: [Region or global]

[Continue filling in all sections...]
```

5. **Save the file**

6. **Test it:**
```
Claude, write a LinkedIn post about [your topic]
```

Claude should now generate content tailored to YOUR context!

### Step 3: Add Voice Samples (Week 2-3)

1. **Navigate to:** `/assets/voice-samples/authentic-voice-samples.md`

2. **Add 2-3 samples** of your natural writing:
   - Email to colleague
   - Newsletter excerpt
   - Article you've written
   - Internal memo

3. **For each sample, note:**
   - Context (where it was written)
   - Tone characteristics
   - Signature phrases

4. **Test voice matching:**
```
Claude, write a post about [topic] in my voice
```

### Step 4: Start Tracking (Month 2+)

As you post on LinkedIn:

1. **After each successful post:**
   - Go to `/assets/examples/high-engagement-posts.md`
   - Copy the post text
   - Note metrics (likes, comments, reach)
   - Analyze why it worked

2. **Claude learns YOUR patterns** and applies them to future content

---

## 🔧 Configuration Options

### Folder Permissions

Ensure Claude has read access to the skill folder:

```bash
# macOS/Linux - Check permissions
ls -la linkedin-thought-leadership/

# Should show read permissions (r) for your user
# Example: -rw-r--r--  (owner can read/write, others can read)
```

### File Encoding

All files should be UTF-8 encoded:

```bash
# macOS/Linux - Verify encoding
file -I linkedin-thought-leadership/SKILL.md

# Should show: text/plain; charset=utf-8
```

### Text Editor Setup

**Recommended settings for editing markdown:**

**VS Code:**
```json
{
  "files.encoding": "utf8",
  "files.eol": "\n",
  "editor.wordWrap": "on",
  "editor.rulers": [100]
}
```

**Sublime Text:**
```json
{
  "default_encoding": "UTF-8",
  "word_wrap": true,
  "rulers": [100]
}
```

---

## 📱 Platform-Specific Notes

### macOS

**Claude Desktop location:**
```
~/Library/Application Support/Claude/skills/
```

**Recommended file manager:** Finder or Forklift

**Text editor:** VS Code, Sublime Text, or TextMate

### Windows

**Claude Desktop location:**
```
%APPDATA%\Claude\skills\
```

**File path note:** Use forward slashes (/) in markdown files, not backslashes (\)

**Recommended text editor:** VS Code, Notepad++, or Sublime Text

### Linux

**Claude Desktop location:**
```
~/.config/Claude/skills/
```

**Recommended text editor:** VS Code, Sublime Text, or Atom

---

## 🔄 Updating the Skill

### For Direct Download Users

1. **Back up your personalization:**
   ```bash
   # Copy your populated assets folder
   cp -r linkedin-thought-leadership/assets assets-backup/
   ```

2. **Download new version** from Releases

3. **Extract and replace:**
   - Replace the skill folder
   - Restore your assets folder

4. **Review CHANGELOG.md** for breaking changes

### For Git Users

```bash
# Save your changes
git add .
git commit -m "Save my personalization"

# Pull latest
git pull origin main

# Resolve any conflicts in SKILL.md
# (Your personalization vs. new features)
```

### For Fork Users

```bash
# Commit your changes
git add .
git commit -m "Save my personalization"

# Fetch upstream
git fetch upstream

# Merge (may require conflict resolution)
git merge upstream/main
```

---

## 🐛 Troubleshooting

### Issue: Claude doesn't recognize the skill

**Solution:**
1. Verify folder structure:
   ```bash
   ls -R linkedin-thought-leadership/
   ```
   Should show SKILL.md, assets/, references/ folders

2. Check SKILL.md has the frontmatter:
   ```markdown
   ---
   name: linkedin-thought-leadership
   description: ...
   ---
   ```

3. Restart Claude Desktop

4. Re-add the skill in Settings

### Issue: Claude ignores my personalization

**Solution:**
1. Verify you filled in PERSONALIZATION SETTINGS in SKILL.md
2. Check file encoding is UTF-8
3. Ensure no syntax errors in your settings (mismatched brackets, quotes)
4. Try asking Claude explicitly: "Using my personalization settings, write..."

### Issue: Asset folders not found

**Solution:**
1. Check folder structure:
   ```bash
   ls linkedin-thought-leadership/assets/
   ```
   Should show: examples/, templates/, frameworks/, etc.

2. Verify folder permissions (readable)

3. Check file paths in SKILL.md are correct

### Issue: Can't edit files

**Solution:**
1. Check file permissions:
   ```bash
   chmod u+w linkedin-thought-leadership/SKILL.md
   ```

2. Ensure file isn't open in another application

3. Use a proper text editor, not a word processor

### Issue: Changes not reflected in Claude

**Solution:**
1. Save the file (Ctrl+S or Cmd+S)
2. Wait 5-10 seconds for Claude to reload
3. Restart Claude if needed
4. Verify you're editing the correct skill folder

---

## 📞 Getting Help

### Self-Service Resources

1. **Read the documentation:**
   - [README.md](README.md) - Overview
   - [PERSONALIZATION-QUICKSTART.md](linkedin-thought-leadership/PERSONALIZATION-QUICKSTART.md) - Setup guide
   - [IMPLEMENTATION-SUMMARY.md](linkedin-thought-leadership/IMPLEMENTATION-SUMMARY.md) - Feature details

2. **Check existing issues:**
   - [GitHub Issues](https://github.com/ktg0066/LinkedIn-skill/issues)
   - Search for your problem

3. **Review troubleshooting** above

### Community Support

1. **GitHub Discussions:**
   - [Ask questions](https://github.com/ktg0066/LinkedIn-skill/discussions)
   - Share experiences
   - Get help from community

2. **Report bugs:**
   - [Open an issue](https://github.com/ktg0066/LinkedIn-skill/issues/new)
   - Include: OS, Claude version, error messages, steps to reproduce

### Direct Support

For installation problems not covered above:
- **Email:** kjell.tore.guttormsen@gmail.com
- Include: OS, installation method, error messages, screenshots

---

## ✅ Installation Checklist

Use this checklist to verify your installation:

- [ ] Downloaded/cloned the skill
- [ ] Added skill to Claude (Desktop or Web)
- [ ] Verified Claude recognizes the skill
- [ ] Filled in PERSONALIZATION SETTINGS in SKILL.md
- [ ] Tested with a simple request
- [ ] Added 2-3 voice samples (optional for Week 1)
- [ ] Read PERSONALIZATION-QUICKSTART.md
- [ ] Bookmarked documentation for reference
- [ ] Joined GitHub Discussions (optional)

---

## 🎓 Next Steps

After installation:

1. **Read the Quick Start:** [PERSONALIZATION-QUICKSTART.md](linkedin-thought-leadership/PERSONALIZATION-QUICKSTART.md)

2. **Create your first post:**
   ```
   Claude, using the LinkedIn skill, write a post about [your topic]
   ```

3. **Start tracking results** in `/assets/examples/`

4. **Join the community** in GitHub Discussions

5. **Star the repository** to stay updated

---

**Installation complete! Ready to build your LinkedIn presence.** 🚀

For questions: [GitHub Discussions](https://github.com/ktg0066/LinkedIn-skill/discussions)
