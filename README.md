# Git & GitHub Classroom Lab

A beginner-friendly HTML/CSS/JavaScript portfolio project for learning version control.

## Before class

Install Git and VS Code, create a GitHub account, and configure your Git identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```

## Teacher setup

1. Create a **public** GitHub repository named `git-github-classroom-lab` (without initializing a README).
2. Extract this starter project, open a terminal in the folder, and run:

```bash
git init
git add .
git commit -m "Initial classroom starter"
git branch -M main
git remote add origin https://github.com/TEACHER_USERNAME/git-github-classroom-lab.git
git push -u origin main
```

3. Share the repository URL with students. For a safe class workflow, students should fork the repository and open pull requests instead of pushing to the teacher's main branch.

## Student lab

### Part 1 — Fork and clone

1. On GitHub, open the teacher's repository and click **Fork** to create a copy under your account.
2. Clone **your fork** (replace `YOUR_USERNAME`):

```bash
git clone https://github.com/YOUR_USERNAME/git-github-classroom-lab-test.git
cd git-github-classroom-lab
git status
```

### Part 2 — Edit and commit

1. In `index.html`, replace `Your Name` with your name.
2. Add a new `<li>` under My Skills.
3. In `style.css`, change a color.
4. Open `index.html` in your browser to check your changes.
5. Run:

```bash
git diff
git add index.html style.css
git commit -m "Personalize portfolio"
git log --oneline -3
```

### Part 3 — Branch and push

```bash
git switch -c feature/my-portfolio
git push -u origin feature/my-portfolio
```

**Note:** In a real project, create the feature branch *before* making edits and commits. The sequence above intentionally introduces commits before branches for the first lesson. Your new branch includes the commit you already made.

### Part 4 — Pull request

1. On your fork's GitHub page, open a pull request from `feature/my-portfolio` to **your fork's `main` branch**. Check the base repository and branch carefully.
2. Review the changed files, write a clear description, and merge the pull request.
3. Update your local main branch:

```bash
git switch main
git pull origin main
```

### Part 5 — Collaboration challenge (optional)

Work in pairs. Student A invites Student B as a collaborator on **Student A's fork**. Student B clones that fork, creates a different feature branch, edits `script.js`, pushes the branch, and opens a pull request to Student A's `main`. Student A reviews and merges it. Avoid editing the same lines until the conflict lesson.

## Submission

- Link to your GitHub fork
- Link to your merged pull request
- Screenshot of `git log --oneline -3`
- Short reflection: What is the difference between Git and GitHub?

## Common troubleshooting

- **Permission denied on push:** Verify `git remote -v` points to your fork, not the teacher's repository, and that you are signed in with the correct GitHub account.
- **Commit identity unknown:** Configure `user.name` and `user.email` as shown above.
- **Nothing to commit:** Check `git status` and confirm files were actually changed and saved.
- **Push rejected:** Run `git pull` on the appropriate branch and resolve any conflicts before retrying. Never use force-push as a beginner shortcut.
