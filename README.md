# WBPH001-10 Lectures

Lecture materials for WBPH001-10, covering mechanics and special relativity.

## Contents

- `Lectures/`: LaTeX source for Lectures 1--15
- `Course_Schedule.tex`: LaTeX source for the course schedule
- `Figures/` and the PDF figures in the repository root: assets required to compile the notes

Compiled lecture and schedule PDFs are intentionally not stored in this repository. The PDF files that remain are source figures required by the LaTeX documents.

To compile a lecture from the repository root, run, for example:

```bash
latexmk -pdf Lectures/Lecture_4.tex
```

This creates `Lectures/Lecture_4.pdf` locally. To compile the schedule, run:

```bash
latexmk -pdf Course_Schedule.tex
```

Corrections and updated versions may be published throughout the course.

## Make your own fork

Please do not work directly from a clone of this repository. Instead, create a **fork** under your own GitHub account:

1. Sign in to GitHub.
2. Click **Fork** near the top-right corner of this repository.
3. Select your own GitHub account as the destination.
4. Keep the default repository name and create the fork.

Your fork is your personal copy. You may edit it, annotate the LaTeX sources, and connect it to services such as Overleaf. You do not have permission to push changes to the official course repository.

Please do not submit pull requests to the official course repository. Student modifications are intended to remain in students' personal forks.

## Recommended branch setup

Keep the `main` branch of your fork as a clean copy of the official notes. Create a separate branch for your own changes:

1. Open your fork on GitHub.
2. Open the branch menu, which initially displays `main`.
3. Enter `my-notes`.
4. Select **Create branch: my-notes from main**.

Make personal edits on `my-notes`, not on `main`. This keeps official course updates separate from your annotations.

## Receiving updates from the course repository

When new lecture material or corrections are published, first update the clean `main` branch of your fork:

1. Open your fork on GitHub.
2. Switch to its `main` branch.
3. Click **Sync fork** and then **Update branch**.

Next, merge the updated `main` branch into `my-notes`. Choose one of the methods below.

### Recommended for beginners: GitHub Desktop

[GitHub Desktop](https://desktop.github.com/) is a free graphical application for Windows and macOS. It lets you use Git without typing terminal commands.

The first time you use it:

1. Install GitHub Desktop and sign in to your GitHub account.
2. In your fork on GitHub, click **Code**, select **Open with GitHub Desktop**, and choose where to save the repository on your computer.

Whenever you want to incorporate new official notes:

1. Synchronize `main` on the GitHub website using **Sync fork → Update branch**, as described above.
2. Open your fork in GitHub Desktop.
3. Select **Current Branch → main**.
4. Click **Fetch origin**, followed by **Pull origin** if that button appears.
5. Select **Current Branch → my-notes**.
6. Click **Fetch origin**, followed by **Pull origin** if that button appears.
7. Open **Current Branch** and select **Choose a branch to merge into my-notes**.
8. Select `main`, then click **Merge main into my-notes**.
9. Click **Push origin** to save the updated `my-notes` branch to your fork on GitHub.

See GitHub's illustrated guide to [getting started with GitHub Desktop](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop).

### Browser-only method

You can also merge the branches entirely on GitHub by opening a pull request **inside your own fork**:

1. Open the **Pull requests** tab of your fork and click **New pull request**.
2. Set the **base repository** to `YOUR-USERNAME/WBPH001-10-Lectures`—your fork, not `daanmeerburg/WBPH001-10-Lectures`.
3. Set the **base branch** to `my-notes` and the **compare branch** to `main`.
4. Create and merge the pull request in your fork.
5. If GitHub offers to delete a branch afterward, do **not** delete `main` or `my-notes`; you will need both for later updates.

This pull request belongs only to your personal fork. Do not create a pull request whose base repository is the official course repository.

### Advanced: terminal commands

If you are comfortable using a terminal, replace `YOUR-USERNAME` with your GitHub username and run:

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

If your changes and an official update modify the same lines, Git will report a merge conflict. You must choose which version to keep before the merge can be completed. See GitHub's instructions for [resolving merge conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts) and [synchronizing a fork](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork).

### New to Git and GitHub?

These introductory resources explain the terminology and basic workflow:

- [Introduction to GitHub](https://github.com/skills/introduction-to-github): an interactive beginner course
- [Getting started with GitHub Desktop](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop): a graphical workflow without terminal commands
- [About Git](https://docs.github.com/en/get-started/using-git/about-git): a short explanation of repositories, commits, branches, and remotes

## Using the notes with Overleaf

If your Overleaf account includes GitHub synchronization:

1. Connect Overleaf to your GitHub account.
2. Create a new Overleaf project from **your fork**, not from the official course repository.
3. After updating your fork, use Overleaf's GitHub integration to pull the new changes into your project.
4. If you edit the project in Overleaf, push those changes only to your own fork.

Overleaf does not synchronize continuously. You must explicitly pull changes from GitHub or push Overleaf changes back to GitHub. GitHub synchronization is an Overleaf premium feature; your institution may provide access. See the [Overleaf GitHub synchronization instructions](https://docs.overleaf.com/integrations-and-add-ons/git-integration-and-github-synchronization/github-synchronization).

If GitHub synchronization is unavailable on your Overleaf account, you can download your fork as a ZIP file and upload it to Overleaf. This works for importing the notes, but future updates must then be transferred manually.

## Repository ownership

The official repository is maintained by the course instructor. Students may freely modify their own forks, but changes in a fork cannot alter the official lecture notes unless the instructor explicitly accepts them.

This public repository is generated from a separately maintained private course repository. Official source changes are made in the private repository and published here automatically.

## Licence

Except where otherwise noted, these lecture materials are copyright Daan Meerburg and licensed under the [Creative Commons Attribution 4.0 International licence](https://creativecommons.org/licenses/by/4.0/).

Third-party material is not covered by this licence unless explicitly indicated. Such material remains subject to its original copyright and licence terms.
