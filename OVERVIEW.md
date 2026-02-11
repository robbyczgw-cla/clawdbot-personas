# Personas Skill - Quick Overview

**Status:** ✅ Production-ready
**Version:** 2.2.2
**Size:** ~204KB (20 personas + docs)
**Created:** 2026-01-20

---

## What Is This?

Transform OpenClaw into 20 specialized AI personalities on demand. Switch from a senior developer to an Italian chef to a fitness coach mid-conversation.

**Example:**
```
You: "Use Dev"
Bot: *becomes senior programmer*

You: "How do I optimize this React component?"
Bot: *gives expert React advice*

You: "Switch to Chef Marco"  
Bot: *becomes passionate Italian chef*

You: "How do I make carbonara?"
Bot: "Ah, la vera carbonara! No cream, mai!..."
```

---

## File Structure

```
personas/
├── README.md              # 📖 User guide (extensive, start here)
├── FAQ.md                 # ❓ Common questions & troubleshooting
├── SKILL.md               # 🎯 OpenClaw skill instructions (loaded on use)
├── skill.json             # ⚙️ Metadata & persona index
├── INTERNAL.md            # 🔧 Developer documentation (for us)
├── OVERVIEW.md            # 📋 This file (quick reference)
├── scripts/
│   └── persona.py         # 🐍 Python CLI handler (NEW in v2.2.0!)
└── data/                  # 📁 20 persona definitions (2-5KB each)
    ├── cami.md            #   🦎 Adaptive chameleon
    ├── dev.md             #   💻 Senior programmer
    ├── chef-marco.md      #   👨‍🍳 Italian cooking expert
    ├── dr-med.md          #   🩺 Medical educator
    └── ... (16 more)
```

---

## Documentation Guide

**For users:**
- **README.md** - Start here! Complete guide to using personas
- **FAQ.md** - Questions, troubleshooting, tips

**For developers/maintainers:**
- **INTERNAL.md** - Architecture, implementation, maintenance
- **creator-workflow.md** - How to implement persona creation feature
- **OVERVIEW.md** - This file (quick reference)

**For OpenClaw:**
- **SKILL.md** - Loaded when skill is invoked
- **skill.json** - Metadata for ClawHub
- **data/*.md** - Individual persona definitions (loaded on demand)

---

## Quick Stats

**Personas:** 20 curated personas

**Categories:**
- Core: 5 personas (Cami, Chameleon Agent, Professor Stein, Dev, Flash)
- Creative: 2 personas (Luna, Wordsmith)
- Curator: 1 persona (Vibe)
- Learning: 3 personas (Herr Müller, Scholar, Lingua)
- Lifestyle: 3 personas (Chef Marco, Fit, Zen)
- Professional: 6 personas (CyberGuard, DataViz, Career Coach, Legal Guide, Startup Sam, Dr. Med)

**CLI Handler:** `scripts/persona.py` (NEW in v2.2.0!)

**Total size:** ~204KB

---

## Key Features

✅ **20 pre-built expert personas**  
✅ **Python CLI handler** (`scripts/persona.py`) — NEW in v2.2.0!  
✅ **Switch mid-conversation**  
✅ **Alias support** (e.g., `chef` → `chef-marco`)  
✅ **State persistence** (remembers active persona)  
✅ **Token-efficient** (load only what you need)  
✅ **Organized by category**  
✅ **Ready for ClawHub publication**

---

## Usage Examples

### Coding Project
```
"Use Dev" → senior dev help
"Switch to Chameleon Agent" → complex architecture
"Use CyberGuard" → security review
```

### Content Creation
```
"Use Wordsmith" → write blog post
"Use Social Pro" → optimize for social media
"Use Canvas" → design graphics
```

### Learning
```
"Use Scholar" → study techniques
"Use Herr Müller" → simple explanations
"Use Lingua" → language practice
```

### Custom Creation
```
"Create a Game Master persona"
→ AI guides through 7-step creation
→ Save to data/game-master.md
→ Use immediately: "Use Game Master"
```

---

## Implementation Notes

**How it works:**
1. User activates persona: `"Use Dev"`
2. OpenClaw reads `data/dev.md` (~3KB)
3. Persona prompt loaded into context
4. AI adopts Dev personality until switched/exited

**Token usage:**
- Index (skill.json): ~250 tokens
- Average persona: ~750 tokens (one-time load)
- Only ONE persona active at a time

**Performance:**
- Activation latency: ~50ms (negligible)
- No response time impact
- Storage: ~204KB total (tiny)

---

## Next Steps

### For End Users
1. Read **README.md** for full guide
2. Try a persona: `"Use Dev"` or `"Use Chef Marco"`
3. Create custom persona: `"Create a [specialty] persona"`
4. Check **FAQ.md** if issues

### For Developers
1. Read **INTERNAL.md** for architecture
2. Review **creator-workflow.md** for implementation
3. Test persona creation workflow
4. Contribute improvements via PR

### For Publishing
1. Verify all files present
2. Test 3-5 personas thoroughly
3. Test creator workflow
4. `clawhub publish` when ready

---

## Common Questions

**Q: Do you load all 20 personas at once?**  
A: No! Only the active persona loads. Token-efficient.

**Q: Can I create custom personas?**  
A: Yes! Guided 7-step creation or edit files directly.

**Q: Can I switch personas mid-conversation?**  
A: Yes! Seamlessly switch anytime.

**Q: Are medical/legal personas giving professional advice?**  
A: No. Educational only. Always consult licensed professionals.

**Q: Can I edit default personas?**  
A: Yes! Edit any file in `data/`. Changes apply immediately.

See **FAQ.md** for 50+ more questions.

---

## Credits

**Original Personas:**
- Source: [Chameleon AI Chat](https://github.com/robbyczgw-cla/Chameleon-AI-Chat)
- License: MIT

**OpenClaw Adaptation:**
- By: robbyczgw-cla
- License: MIT

---

## Version History

**v1.0.0** (2026-01-20)
- Initial release
- 20 default personas from Chameleon AI
- Creator workflow
- Comprehensive documentation
- Ready for ClawHub

---

**Built with 🦎 by the Chameleon community**
