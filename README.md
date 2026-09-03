# 02369 - Software processes and patterns Notes

Personal notes for **02369 Software processes and patterns**. Structured as an [Obsidian](https://obsidian.md/) vault, but works as plain Markdown.

## Usage

### Option 1: Download Only
Download the ZIP archive from GitHub, extract it, and open the folder in Obsidian via **Open folder as vault**.

### Option 2: Fork & Sync (Recommended)
Fork this repository to receive material updates while keeping your own notes.

1. **Clone your fork:**
```bash
git clone [https://github.com/YOUR_USERNAME/02369-software-processes-and-patterns-notes.git](https://github.com/YOUR_USERNAME/02369-software-processes-and-patterns-notes.git)
cd 02369-software-processes-and-patterns-notes
```

2. **Set upstream repository:**
```bash
git remote add upstream [https://github.com/lassedtu/02369-software-processes-and-patterns-notes.git](https://github.com/lassedtu/02369-software-processes-and-patterns-notes.git)
```


3. **Open in Obsidian:**
	Open Obsidian and select **Open folder as vault** -> select the cloned directory.

## Syncing Updates

Save your personal changes, fetch updates, and merge:

```bash
# Save your notes
git add .
git commit -m "Update personal notes"

# Pull original repo updates
git fetch upstream
git merge upstream/main
git push origin main
```

If merge conflicts occur, resolve the `<<<<<<<` markers in your text editor, commit, and push.

---

Contributions and fixes welcome via pull requests or issues.
