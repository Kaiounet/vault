# Zettelkasten Knowledge Base

A personal knowledge management system built using the Zettelkasten method in Obsidian.

---

## 📚 Table of Contents

- [What is Zettelkasten?](#what-is-zettelkasten)
- [Why Zettelkasten?](#why-zettelkasten)
- [Core Principles](#core-principles)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Note Types](#note-types)
- [Workflow](#workflow)
- [Naming Conventions](#naming-conventions)
- [Linking Strategy](#linking-strategy)
- [Templates](#templates)
- [Best Practices](#best-practices)
- [Tools & Plugins](#tools--plugins)

---

## 🧠 What is Zettelkasten?

Zettelkasten (German for "slip box") is a knowledge management method developed by sociologist Niklas Luhmann. It's a system for taking notes, organizing ideas, and building interconnected knowledge over time.

Rather than organizing notes hierarchically in folders, Zettelkasten creates a **network of ideas** where each note is:

- **Atomic**: Contains one clear idea
- **Connected**: Linked to related notes
- **Permanent**: Written in your own words for long-term understanding

The power comes from discovering unexpected connections between ideas as your knowledge base grows.

---

## 💡 Why Zettelkasten?

### Problems with Traditional Note-Taking

- Notes sit isolated in folders, never revisited
- Information is organized by source, not by idea
- Hard to see connections between different topics
- Knowledge doesn't compound over time

### Benefits of Zettelkasten

- **Emergence**: New insights arise from connecting existing notes
- **Retention**: Writing in your own words strengthens understanding
- **Creativity**: Random exploration leads to unexpected discoveries
- **Productivity**: Build a library of ideas ready for projects
- **Learning**: Forces deep processing of information

---

## 🎯 Core Principles

### 1. Atomicity

Each note contains exactly **one idea**. If you're writing "and" or "also," you probably need two notes.

**Good**: A note about "Cognitive load reduces decision quality"  
**Bad**: A note about "Psychology concepts I learned today"

### 2. Connectivity

Notes gain value through links to other notes. Always ask: "What does this remind me of?"

### 3. Own Words

Never copy-paste. Rewrite ideas in your own language to ensure understanding.

### 4. Progressive Development

Your knowledge base grows organically. Start small, link consistently, trust the process.

---

## 📁 Repository Structure

```
zettelkasten/
├── README.md                           # This file
├── 00-Inbox/                           # Unprocessed fleeting notes
├── 01-Literature/                      # Source notes and references
├── 02-Permanent/                       # Your main knowledge base
├── 03-Projects/                        # Active projects
├── 04-Archive/                         # Completed projects
├── 99-Assets/                          # Images, PDFs, attachments
└── 99-Templates/                       # Note templates
    ├── _Fleeting.md
    ├── _Index.md
    ├── _Literature.md
    ├── _Permanent-Simple.md
    ├── _Permanent-Standard.md
    └── _Project.md
```

### Folder Purposes

**Numbering System**: Folders are prefixed with numbers to control sort order and create a logical flow through your knowledge base.

- **00-Inbox**: Temporary storage for fleeting notes and quick captures. Process regularly to keep this folder clean.
- **01-Literature**: Notes from books, articles, videos, podcasts with full citations and bibliographic information.
- **02-Permanent**: Your core knowledge base of atomic, interconnected notes. This is where the magic happens.
- **03-Projects**: Active work-in-progress that draws on your permanent notes. Research, articles, presentations currently being developed.
- **04-Archive**: Completed projects moved from `03-Projects/`. Keeps active projects folder clean while preserving finished work for reference.
- **99-Assets**: Images, PDFs, documents, and other attachments referenced in your notes.
- **99-Templates**: Reusable note structures prefixed with `_` for easy identification and consistency.

### Why This Structure?

- **Numbered folders** appear in a consistent order across all devices and file browsers
- **00-Inbox** comes first as your capture point and processing queue
- **Sequential flow**: Inbox → Literature/Permanent → Projects → Archive
- **99-** prefix pushes support folders (Assets, Templates) to the bottom
- **Template files with `_` prefix** sort to the top within the Templates folder
- **Clear separation** between active work (03-Projects) and completed work (04-Archive)

---

## 🚀 Getting Started

### Prerequisites

1. Install [Obsidian](https://obsidian.md)
2. Clone or download this repository
3. Open the folder in Obsidian as a vault

### Initial Setup

1. **Configure Templates**
    
    - Go to Settings → Core Plugins → Enable "Templates"
    - Set Templates folder location to `99-Templates/`
    - Assign hotkey (e.g., `Ctrl/Cmd + T`)
2. **Recommended Settings**
    
    - Enable WikiLinks: Settings → Files & Links → Use [[Wikilinks]]
    - Auto-pair brackets: Settings → Editor → Auto pair brackets
    - Default note location: Settings → Files & Links → Set to `00-Inbox/`
3. **Git Setup** (for version control)
    
    - Initialize repository: `git init`
    - Create `.gitkeep` files in empty directories
    - Add `.gitignore` if needed
    - Commit structure: `git add . && git commit -m "Initial repository structure"`
4. **Optional Tools**
    
    - Excalidraw: For creating diagrams and visual notes within Obsidian

### Your First Note

1. Press `Ctrl/Cmd + N` to create a new note in `00-Inbox/`
2. Insert the "_Fleeting" template (`Ctrl/Cmd + P`)
3. Write down a quick idea or thought
4. Later, process it into a permanent note:
    - Create new note in `02-Permanent/` with timestamp ID format: `YYYYMMDDHHmm Description.md`
    - Use "_Permanent-Simple" template
    - Write the idea in your own words
    - Link to related concepts

---

## 📝 Note Types

### 1. Fleeting Notes

**Purpose**: Quick captures of ideas, thoughts, observations  
**Location**: `00-Inbox/`  
**Lifespan**: Temporary - process within 48 hours  
**Template**: `_Fleeting.md`

**Example**: "Interesting point from podcast about habit formation"

### 2. Literature Notes

**Purpose**: Summaries and insights from external sources  
**Location**: `01-Literature/`  
**Lifespan**: Permanent reference material  
**Template**: `_Literature.md`

**Example**: "Literature - Atomic Habits by James Clear"

### 3. Permanent Notes

**Purpose**: Your main knowledge base - atomic ideas in your own words  
**Location**: `02-Permanent/`  
**Lifespan**: Permanent and evergreen  
**Templates**: `_Permanent-Standard.md` or `_Permanent-Simple.md`

**Example**: "202311171430 Habits form through cue-routine-reward loops"

### 4. Index Notes

**Purpose**: Topic hubs that organize related permanent notes  
**Location**: `02-Permanent/` (stored alongside permanent notes)  
**Lifespan**: Grows over time  
**Template**: `_Index.md`

**Example**: "Index - Behavioral Psychology"

**Note**: Index notes are hub notes that don't need a separate folder. They live in your permanent notes and use the "Index -" prefix in their title to distinguish them.

### 5. Project Notes

**Purpose**: Active work that draws on your permanent notes  
**Location**: `03-Projects/`  
**Lifespan**: Until project completion, then move to `04-Archive/`  
**Template**: `_Project.md`

**Example**: "Project - Building Better Habits Article"

---

## 🔄 Workflow

### Daily Practice

#### Morning (5 minutes)

1. Review yesterday's fleeting notes in `00-Inbox/`
2. Quick capture any overnight thoughts

#### During the Day

- Capture fleeting notes as ideas arise
- Use mobile Obsidian or quick capture tool
- Don't worry about organization

#### Evening (15-20 minutes)

1. **Process Inbox**
    
    - Review fleeting notes in `00-Inbox/`
    - Decide: delete, develop into permanent note, or convert to literature note
2. **Create Permanent Notes**
    
    - Take one fleeting or literature note
    - Create new note in `02-Permanent/` with timestamp ID
    - Write it in your own words
    - Ask: "What's the ONE idea here?"
3. **Link and Connect**
    
    - Find 2-3 related permanent notes
    - Add links in both directions
    - Update or create relevant index notes (using `_Index.md` template)
4. **Explore**
    
    - Click through random backlinks
    - Browse the graph view
    - Note unexpected connections

### Weekly Review (30 minutes)

- Clear out `00-Inbox/` completely
- Review recent permanent notes in `02-Permanent/`
- Update index notes
- Move completed projects from `03-Projects/` to `04-Archive/`
- Clean up and organize `99-Assets/` if needed

---

## 🏷️ Naming Conventions

### Permanent Notes

**Format**: `YYYYMMDDHHmm Description.md`

**Examples**:

- `202311171430 Spaced repetition improves retention.md`
- `202311171445 Dopamine drives motivation not pleasure.md`

**Why timestamps?**

- Ensures unique IDs
- Preserves chronological order
- Makes referencing easy
- No naming conflicts

### Literature Notes

**Format**: `Literature - Author Title.md`

**Examples**:

- `Literature - Clear Atomic Habits.md`
- `Literature - Kahneman Thinking Fast and Slow.md`

### Index Notes

**Format**: `Index - Topic.md`

**Examples**:

- `Index - Learning Science.md`
- `Index - Product Management.md`

### Project Notes

**Format**: `Project - Description.md`

**Examples**:

- `Project - Learning System Redesign.md`
- `Project - Q4 Strategy Presentation.md`

---

## 🔗 Linking Strategy

### Types of Links

#### Direct Links

Connect notes that directly relate:

```markdown
This builds on [[202311171430 Previous idea]]
```

#### Contextual Links

Explain the relationship:

```markdown
This contrasts with [[202311151200 Opposing view]] because...
```

#### Index Links

Connect to topic hubs:

```markdown
Related: [[Index - Cognitive Psychology]]
```

### When to Link

- When one idea builds on another
- When ideas contrast or conflict
- When an example illustrates a concept
- When you think "this reminds me of..."

### Link Density

Aim for **3-5 meaningful links** per permanent note. Too few and notes become isolated. Too many and links lose significance.

---

## 📋 Templates

All templates are in the `99-Templates/` folder and are prefixed with `_` for easy identification:

- `_Fleeting.md` - Quick capture template
- `_Index.md` - Topic hub template
- `_Literature.md` - Source note template
- `_Permanent-Simple.md` - Streamlined permanent note
- `_Permanent-Standard.md` - Detailed permanent note
- `_Project.md` - Project tracking template

### Using Templates

1. Create new note (`Ctrl/Cmd + N`)
2. Insert template (`Ctrl/Cmd + P`)
3. Fill in placeholders
4. Replace `{{date}}` and `{{time}}` with current values

### Template Variables

- `{{date}}`: Current date in YYYYMMDD format
- `{{time}}`: Current time in HHMM format
- `{{title}}`: Your note title

### Customizing Templates

Feel free to modify templates in `99-Templates/` to fit your workflow. Common customizations:

- Add custom tags
- Include specific sections for your domain
- Adjust metadata fields
- Change formatting style

Remember: Templates with `_` prefix will always sort to the top of the folder for easy access.

---

## ✅ Best Practices

### Do's

- ✅ Write in complete sentences
- ✅ Use your own words
- ✅ Link generously and meaningfully
- ✅ Keep notes atomic (one idea)
- ✅ Process inbox regularly
- ✅ Review and update existing notes
- ✅ Follow random links for serendipity

### Don'ts

- ❌ Copy-paste from sources
- ❌ Create notes "just in case"
- ❌ Over-organize with complex folder structures
- ❌ Let fleeting notes pile up unprocessed
- ❌ Write novel-length notes
- ❌ Ignore fleeting notes for weeks
- ❌ Use tags as a substitute for links

### Common Pitfalls

**Problem**: Inbox overflow  
**Solution**: Set a daily processing time, keep `00-Inbox/` under 20 notes

**Problem**: Notes too long  
**Solution**: Split when you write "and" or "also"

**Problem**: No connections forming  
**Solution**: Browse graph weekly, force yourself to find 3 links per note

**Problem**: Perfectionism  
**Solution**: Remember: seedling notes can grow into evergreens later

**Problem**: Can't decide where to put a note  
**Solution**: The numbered folder structure guides you - fleeting notes in `00-Inbox/`, processed notes in `02-Permanent/`

---

## 🛠️ Tools & Setup

### Core Obsidian Features

**Templates** (Built-in)

- Insert note templates quickly
- Maintain consistency across note types
- Configure in Settings → Core Plugins → Templates

**Graph View** (Built-in)

- Visualize connections between notes
- Discover clusters and patterns
- Filter by tags or folders

**Backlinks** (Built-in)

- See which notes link to the current note
- Discover unexpected connections
- Build bidirectional links

**Outgoing Links** (Built-in)

- See what the current note links to
- Ensure proper connections
- Track reference completeness

### Additional Tools

**Git** (Version Control)

- Track changes to your knowledge base
- Sync across devices
- Backup and version history
- Commit regularly with meaningful messages

**Excalidraw** (Visual Notes)

- Create diagrams and sketches
- Visual thinking and mind mapping
- Embed drawings in notes
- Useful for complex concepts and relationships

### Workflow Integration

**Daily Git Commits**

```bash
# After your daily review
git add .
git commit -m "Daily update: processed inbox, added 3 permanent notes"
git push
```

**Using Excalidraw for Concepts**

- Create visual representations of complex ideas
- Link Excalidraw files from permanent notes
- Store in `99-Assets/` for organization

---

## 🌱 Growing Your Zettelkasten

### First Month

- **Goal**: Build the habit
- Create 1-2 permanent notes daily
- Focus on consistency over quality
- Don't worry about connections yet

### Months 2-3

- **Goal**: Develop your voice
- Notes become easier to write
- Start seeing recurring themes
- Create first index notes

### Months 4-6

- **Goal**: Leverage the network
- Unexpected connections emerge
- Use notes for projects
- Graph becomes meaningful

### Beyond 6 Months

- **Goal**: Trust the system
- Your "second brain" becomes reliable
- Writing projects draw on existing notes
- New ideas naturally connect to old ones

---

## 📊 Success Metrics

Track these to ensure healthy growth:

- **Notes created per week**: Consistency matters more than volume
- **Average links per note**: Aim for 3-5
- **Inbox processing frequency**: Clear at least 2x per week
- **Surprise connections found**: Weekly discoveries mean it's working
- **Projects using notes**: Your knowledge should feed your work
- **Archive growth**: Completed projects show productive use of your Zettelkasten

---

## 🤝 Contributing

This is a personal knowledge base, but you can:

- Fork this structure for your own use
- Suggest template improvements
- Share workflow optimizations
- Report structural issues

---

## 📝 License

This structure and templates are provided as-is for personal use. Feel free to adapt and modify for your own knowledge management system.

---

## 🙋 Questions?

Remember: The best Zettelkasten is the one you actually use. Start simple, stay consistent, and let the system grow naturally.

**Key takeaway**: Write one atomic note, link it to two others, repeat daily. Everything else is details.

---

_Last Updated: November 2025_ _Version: 1.0_