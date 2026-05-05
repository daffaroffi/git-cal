# git-cal

git-cal is a simple tool to view your Git contribution calendar directly in your terminal, similar to the contribution graph on a GitHub profile.

### Modern Features
This tool has been updated to work with legacy repositories and modern workspaces:
*   **Workspace Auto-Scan**: Point to a root folder, and the script will automatically find and aggregate data from all Git repositories inside it.
*   **Time Travel**: View contribution history from any year or period using the --since and --anchor options.
*   **Aggregate View**: Combine history from multiple repositories into a single calendar view.
*   **Zero Dependencies**: Works with standard Perl available on most Linux systems.

---

### Usage

#### 1. Basic Usage
Run inside any Git repository:
```bash
./git-cal
```

#### 2. Scan an Entire Workspace
If you have a folder containing multiple projects (e.g., /home/user/projects), you can view the aggregate activity of all of them:
```bash
./git-cal "/home/user/projects/"
```

#### 3. View Old History
To view contributions from a specific past period, such as the year 2015:
```bash
./git-cal --since="15 years" --anchor="2015-12-31"
```

#### 4. Filter by Author
```bash
./git-cal --author="Your Name"
```

---

### Installation
Ensure the git-cal file has execution permissions:
```bash
chmod +x git-cal
```

---

### Credits and License
This tool is a modernized version of the original project created by:
*   **Original Author**: Karthik Katooru ([@k4rthik](https://github.com/k4rthik))
*   **License**: MIT License

