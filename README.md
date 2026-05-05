# git-cal

### Description
`git-cal` is a simple script to view your git contribution calendar (similar to GitHub's contribution graph) directly in your terminal.

![screenshot with black theme](https://raw.github.com/k4rthik/git-cal/master/screenshots/img1.png)

### Features
*   **GitHub-style Calendar**: View commits over the past year in a 53x7 grid.
*   **Multiple Formats**: Support for ANSI colors, Unicode, and ASCII.
*   **Time Travel**: Use `--since` and `--anchor` to view history from any point in time.
*   **Author Filtering**: Filter contributions by a specific author.
*   **Zero Dependencies**: Works with standard Perl (core modules only).

---

### Installation

#### Option 1: Quick Run (No Install)
Simply clone and run:
```bash
chmod +x git-cal
./git-cal
```

#### Option 2: Local Install
```bash
perl Makefile.PL PREFIX=~/.local
make
make install
```

---

### Usage

#### Basic Usage
View contributions for the last 13 months in the current repository:
```bash
git-cal
```

#### Time Travel (Legacy Projects)
If you want to see contributions from a specific year or period:
```bash
# View contributions in 2015
git-cal --since="15 years" --anchor="2015-12-31"

# View the last 2 years
git-cal --since="2 years"
```

#### Customization
```bash
# Use Unicode blocks instead of ANSI colors
git-cal --unicode

# Filter by author
git-cal --author="John Doe"

# Show only specific months (e.g., 1=Jan, 2=Feb)
git-cal --period=2
```

#### Pro Tip: View All Projects
If you have a folder with multiple projects and want to see aggregate activity, you can use this command:
```bash
# 1. Collect all timestamps into a file
find /path/to/projects/ -maxdepth 2 -name .git -type d -exec git --git-dir={} log --all --pretty=format:"%at" \; > /tmp/all_commits.txt

# 2. View the calendar using the collected file
git-cal --file /tmp/all_commits.txt
```

---

### Git Config
You can save your preferences in your git config:
```bash
git config --global calendar.format unicode
git config --global calendar.since "1 year"
```

### License
MIT License

