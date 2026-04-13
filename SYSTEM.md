# Writing System — Manufacturing × AI × Product Development

A fully automated, assembly-line publishing pipeline for long-form articles on the intersection of manufacturing, AI, and product development (ERP, MES, factory automation, robotics, supply chain systems, and more).

---

## How It Works

Articles move through a staged pipeline, much like a product moving through a factory floor. Each stage is handled by a specialized agent. The pipeline runs daily. Three stages require a human checkpoint (you) before advancing.

```
[IDEA] → [RESEARCH] → [OUTLINE] ──► HUMAN REVIEW ──► [DATA] → [WRITING] → [DRAFT] ──► HUMAN REVIEW ──► [EDITING] → [FINAL] ──► HUMAN REVIEW ──► [PUBLISHING] → [MARKETING] → [PUBLISHED]
```

### Stage Descriptions

| Stage | Agent | Human? | Output |
|-------|-------|--------|--------|
| `idea` | — | You add idea | `articles/_ideas/<slug>.md` |
| `research` | Research Agent | — | `articles/_research/<slug>/` |
| `outline` | Outline Agent | **Review outline** | `articles/_outlines/<slug>.md` |
| `data` | Data Agent | — | `data/analyses/<slug>/` |
| `writing` | Writing Agent | — | `articles/_drafts/<slug>.md` |
| `editing` | Editing Agent | **Review draft** | `articles/_drafts/<slug>_edited.md` |
| `final` | — | **Final approval** | `articles/_final/<slug>.md` |
| `publishing` | Publishing Agent | — | `articles/_published/<slug>.md` |
| `marketing` | Marketing Agent | — | `analytics/reports/<slug>_marketing.md` |

### Human Review Checkpoints

The pipeline pauses at three points:

1. **After Outline** — Review the structure and angle before research becomes writing.
2. **After Editing** — Review the polished draft before publishing.
3. **After Final** — Final approval gate before it goes out.

To advance an article through a review checkpoint, edit its entry in `pipeline/queue.json` and change the stage from `*_review` to `*_approved`. Then the next daily run picks it up.

Or run the pipeline manually anytime with:
```
claude "Run the writing pipeline per SYSTEM.md — check pipeline/queue.json and advance all eligible articles one stage."
```

---

## Directory Structure

```
Writings/
├── SYSTEM.md                    # This file
├── articles/
│   ├── _ideas/                  # Raw article briefs (one .md per article)
│   ├── _research/               # Research notes (one folder per article)
│   ├── _outlines/               # Structured outlines
│   ├── _drafts/                 # Working drafts
│   ├── _review/                 # Checkpoint files for human review
│   ├── _final/                  # Final approved articles
│   └── _published/              # Published, formatted output
├── data/
│   ├── analyses/                # Data analyses and charts per article
│   └── datasets/                # Reusable source datasets
├── images/
│   ├── generated/               # AI-generated images (by article slug)
│   └── collected/               # Curated images with attribution notes
├── templates/                   # Document templates for each stage
├── agents/                      # Agent system prompts for each stage
├── pipeline/
│   ├── queue.json               # Article pipeline state (THE source of truth)
│   └── config.json              # System configuration
└── analytics/
    └── reports/                 # Per-article marketing and performance reports
```

---

## Adding a New Article Idea

1. Copy `templates/idea.md` into `articles/_ideas/<your-slug>.md`
2. Fill in the title, hook, key questions, and target audience
3. Add an entry to `pipeline/queue.json` with stage `"idea"`
4. The next daily pipeline run will pick it up and start research

---

## Cloud Sync

This system uses Git for version control and cloud sync.

**Initial setup (one time):**
```bash
cd /Users/exiang/Writings
git init
git add .
git commit -m "Initial writing system setup"
# Create a private repo on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/writings.git
git push -u origin main
```

**The daily pipeline agent commits and pushes after each run automatically.**

---

## Topic Focus Areas

Per `pipeline/config.json`, the system focuses on:
- ERP systems and digital transformation in manufacturing
- MES (Manufacturing Execution Systems)
- Factory automation and robotics
- AI/ML applications in supply chain and operations
- Industrial IoT and smart factory concepts
- Product lifecycle management (PLM)
- Lean/Six Sigma meets AI
- Founders and operators building in the industrial space

---

## Scheduling

The daily pipeline runs via a scheduled Claude Code agent. See `agents/pipeline_runner.md` for the full agent prompt. The schedule is configured to run at 8:00 AM daily.
