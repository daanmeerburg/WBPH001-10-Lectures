# WBPH001-10 Lectures

Lecture materials for WBPH001-10, covering mechanics and special relativity. Corrections and updated versions may be published throughout the course.

## Choose how you want to use the notes

### Option 1 — Read the ready-made PDFs

This is the simplest option and is recommended if you only want to read the lecture notes.

- Ready-to-read PDFs are provided on Brightspace and in [`lecture_pdf/`](lecture_pdf/).
- You do not need GitHub, Git, LaTeX, or Overleaf.
- Updated PDFs will be posted on Brightspace when appropriate.

### Option 2 — Make editable notes in Overleaf

Choose this option if you want to annotate or change the LaTeX source without installing LaTeX on your computer.

1. Sign in to GitHub and create a **fork** of this repository under your own account.
2. Import your fork into Overleaf.
3. Make personal edits only in your own fork or Overleaf project.

Overleaf's GitHub synchronization is a premium feature, although your institution may provide access. If it is available, Overleaf can pull updates from and push your edits to your fork. Synchronization is not continuous: you must explicitly initiate each pull or push. See the [Overleaf GitHub synchronization instructions](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github-synchronization).

Without GitHub synchronization, download your fork as a ZIP file and upload it to Overleaf. This requires no local software, but later course updates must be transferred manually.

### Option 3 — Work and compile locally

Choose this option if you are comfortable using Git and LaTeX locally. Before starting, install:

- [Git](https://git-scm.com/downloads), or [GitHub Desktop](https://desktop.github.com/) if you prefer a graphical application;
- a LaTeX distribution containing `latexmk`:
  - Windows: [MiKTeX](https://miktex.org/download) or [TeX Live](https://tug.org/texlive/);
  - macOS: [MacTeX](https://tug.org/mactex/);
  - Linux: TeX Live through your distribution's package manager.

The Git commands below work on macOS and Linux terminals and on Windows in Git Bash. The individual `git` commands also work in PowerShell. GitHub Desktop provides a graphical alternative to most terminal commands.

## Repository contents

- `Lectures/`: LaTeX source for Lectures 1–15
- `lecture_pdf/`: automatically generated PDFs for Lectures 1–15 and the course schedule
- `Course_Schedule.tex`: LaTeX source for the course schedule
- `Figures/` and the PDF figures in the repository root: assets required to compile the notes

The files in `lecture_pdf/` are rebuilt automatically whenever lecture sources or the course schedule change. Other PDFs in the repository are source figures required to compile the LaTeX documents.

From the repository root, compile a lecture with, for example:

```bash
latexmk -pdf Lectures/Lecture_4.tex
```

This creates `Lectures/Lecture_4.pdf`. Compile the schedule with:

```bash
latexmk -pdf Course_Schedule.tex
```

## Fork the repository before making changes

Please do not work directly from a clone of the official repository. Instead:

1. Sign in to GitHub.
2. Click **Fork** near the top-right of this repository.
3. Select your GitHub account as the destination.
4. Keep the default repository name and create the fork.

Your fork is your personal copy. Your changes cannot alter the official course repository. Please do not submit pull requests to the official repository.

## Keep official updates separate from your notes

The recommended branch arrangement in your fork is:

- `main`: a clean copy of the official course notes;
- `my-notes`: your annotations and personal changes.

To create the personal branch in the browser:

1. Open your fork on GitHub.
2. Open the branch menu, which initially displays `main`.
3. Enter `my-notes`.
4. Select **Create branch: my-notes from main**.

You can continue receiving course updates in your annotated version. First synchronize `main` with the official repository, and then merge the updated `main` into `my-notes`:

```text
official repository → your fork/main → your fork/my-notes
```

This update is not automatic. If your annotations and an official update change the same lines, Git will ask you to resolve a merge conflict by choosing what to keep.

## Update and merge using the browser

First update the clean branch:

1. Open your fork on GitHub and switch to `main`.
2. Click **Sync fork**, followed by **Update branch**.

Then merge those updates into your annotated branch using a pull request inside your fork:

1. Open the **Pull requests** tab of your fork and click **New pull request**.
2. Set the **base repository** to `YOUR-USERNAME/WBPH001-10-Lectures`, not the official repository.
3. Set the **base branch** to `my-notes` and the **compare branch** to `main`.
4. Create and merge the pull request.
5. Do not delete `main` or `my-notes` afterward; both are needed for future updates.

## Update and merge using GitHub Desktop

The first time:

1. Install GitHub Desktop and sign in.
2. In your fork on GitHub, select **Code → Open with GitHub Desktop**.

For later course updates:

1. Synchronize `main` on GitHub using **Sync fork → Update branch**.
2. In GitHub Desktop, select **Current Branch → main** and click **Fetch origin**, then **Pull origin** if offered.
3. Select **Current Branch → my-notes** and fetch or pull that branch too.
4. Select **Current Branch → Choose a branch to merge into my-notes**.
5. Select `main`, click **Merge main into my-notes**, and then **Push origin**.

See GitHub's [GitHub Desktop guide](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop).

## Update and merge using a terminal

Replace `YOUR-USERNAME` with your GitHub username:

```bash
git clone https://github.com/YOUR-USERNAME/WBPH001-10-Lectures.git
cd WBPH001-10-Lectures
git switch main
git pull origin main
git switch my-notes
git pull origin my-notes
git merge main
git push origin my-notes
```

The cloning commands are needed only once. For subsequent updates, start with `git switch main` inside the existing local folder.

For help, see:

- [Introduction to GitHub](https://github.com/skills/introduction-to-github)
- [About Git](https://docs.github.com/en/get-started/using-git/about-git)
- [Synchronizing a fork](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork)
- [Resolving merge conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts)

## Repository ownership

The official repository is maintained by the course instructor. Student modifications remain in personal forks unless the instructor explicitly accepts them.

This public repository is generated from a separately maintained private course repository. Official source changes are made in the private repository and published here automatically.

## Licence

Except where otherwise noted, these lecture materials are copyright Daan Meerburg and licensed under the [Creative Commons Attribution 4.0 International licence](https://creativecommons.org/licenses/by/4.0/).

Third-party material is not covered by this licence unless explicitly indicated. Such material remains subject to its original copyright and licence terms.
