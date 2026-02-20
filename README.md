# FROG Task Base - Dedicated Obsidian Vault

**Location:** `/home/scott/dev/frog-taskbase/`

A dedicated, focused Obsidian vault for managing THE FROG project (Team Task Dashboard) and related initiatives.

---

## 🚀 Quick Start

### 1. Open in Obsidian
```bash
# Open Obsidian → Vault Switcher → Open Folder as Vault
# Select: ~/dev/frog-taskbase
```

### 2. Install Plugins
Recommended community plugins:
- **Tasks** - Checkbox tracking, filters, sorting
- **Database** - Relation views (optional but powerful)
- **Kanban** - Visual workflow
- **Dataview** - Dynamic queries (optional)
- **Obsidian Git** - Auto-commit (optional)
- **Templater** - Quick task creation (optional)
- **Calendar** - Date navigation (optional)

Install via: Settings → Community Plugins

### 3. Start Here
Open: **00 - HOME.md** (vault home page)

---

## 📂 Vault Structure

```
frog-taskbase/
├── 00 - HOME.md              (Start here)
├── README.md                 (This file)
├── Master Task List.md       (Overview of all tasks)
├── Projects/
│   ├── FROG/
│   │   └── Phase 1 Tasks.md  (Database + Backend + Auth)
│   ├── Agent Battle Arena/
│   │   └── Phase 1 Tasks.md  (Sponsorship + Sandbox)
│   └── botb.cloud/
│       └── Features.md        (Coming soon)
├── Agents/
│   ├── Logic G Tasks.md      (Backend developer)
│   ├── Bug Killa Tasks.md    (QA tester)
│   ├── Deep Dive Tasks.md    (Researcher/documentor)
│   ├── Vibe Lord Tasks.md    (Designer/thinker)
│   ├── Pixel Pusha Tasks.md  (Frontend developer)
│   ├── Bossman Tasks.md      (PM/admin)
│   └── Run CMD Tasks.md      (You - orchestrator)
├── Archives/                 (Completed sprints)
└── .obsidian/               (Vault config - auto-managed)
```

---

## 🎯 How It Works

### Task Lifecycle

```
READY → IN PROGRESS → REVIEW → COMPLETE → ARCHIVE
  ↑                              ↓
  └──────────────────────────────┘
         (Fix & retry)
```

### Status Labels
- 🟦 **READY** — Prerequisites met, ready to start
- 🟨 **IN PROGRESS** — Agent actively working
- 🟧 **REVIEW** — Code/docs ready for validation
- 🟩 **COMPLETE** — Approved & closed
- ⬜ **BLOCKED** — Waiting on something

### Vault Views

#### 1. Graph View (Big Picture)
- Shows connections between projects, tasks, agents
- Highlight nodes to see dependencies
- Useful for: Understanding the system

#### 2. Kanban View (Workflow)
- Drag tasks between columns (READY → IN PROGRESS → REVIEW → COMPLETE)
- See progress at a glance
- Useful for: Daily standups

#### 3. Calendar View (Timeline)
- See due dates
- Jump to tasks by date
- Useful for: Sprint planning

---

## 🔗 Linking Convention

All task lists use Obsidian `[[]]` links:

```markdown
# Project link
[[../Projects/FROG/Phase 1 Tasks]]

# Agent link
[[../Agents/Logic G Tasks]]

# Master link
[[Master Task List]]
```

Obsidian auto-resolves these, making navigation seamless.

---

## 📊 Querying Tasks (Dataview)

Once you have Dataview plugin, create queries like:

```markdown
# Show all READY tasks
```dataview
LIST 
FROM "Projects" OR "Agents"
WHERE contains(Status, "READY")
```

# Show all tasks assigned to Logic G
```dataview
LIST
FROM "Projects" OR "Agents"
WHERE contains(Assigned, "Logic G")
```
```

---

## ✅ Weekly Workflow

### Monday - Sprint Planning
1. Open [[Master Task List]]
2. Review completed tasks from last week
3. Review upcoming tasks
4. Update due dates if needed
5. Communicate with agents

### Daily - Standup
1. Each agent opens their task list
2. Reports status on current subtask
3. Flags any blockers
4. Moves task card on Kanban

### Friday - Sprint Review
1. Gather all completed subtasks
2. Generate sprint report
3. Archive completed project phase (if applicable)
4. Plan next sprint

---

## 🛠️ Customization

### Change Theme
Settings → Appearance → Theme → Select theme
(Recommended: "Minimal" for clean task view)

### Disable Plugins
Settings → Community Plugins → Toggle off
(You can keep only what you use)

### Add New Projects
1. Create folder: `Projects/[Project Name]/`
2. Create `Phase 1 Tasks.md`
3. Link from [[Master Task List]]
4. Create agent task lists as needed

---

## 💾 Backup & Sync

### Local Git (Recommended)
```bash
cd ~/dev/frog-taskbase
git init
git add .
git commit -m "FROG Task Base v1"
git remote add origin https://github.com/sries74/frog-taskbase
git push
```

### Obsidian Sync (Optional)
- Requires Obsidian account (~$10/month)
- Auto-syncs across devices
- Encrypted on Obsidian's servers

---

## 🐛 Troubleshooting

### Links not working
- Check path is correct: `[[../../Projects/FROG/Phase 1 Tasks]]`
- Verify file exists in folder
- Try: Cmd+K → search file name → insert link

### Plugins not showing
- Settings → Community Plugins → Browse
- Search by name (e.g., "tasks")
- Install + Enable

### Vault locked/corrupted
- Close Obsidian
- Delete `.obsidian/workspace` file
- Reopen vault

---

## 📞 Questions?

Refer to:
- [[00 - HOME]] — Quick navigation
- [[Master Task List]] — What to work on
- Your agent task list — Your specific work
- Project folder — Project context

---

## 📝 Version History

- **v1.0** — Feb 19, 2026
  - Initial vault structure created
  - 3 projects set up
  - 7 agent task lists created
  - Master task list active

---

**Open [[00 - HOME]] to get started!** 🚀
