# WBPH001-10 Lectures

Lecture materials for WBPH001-10, covering mechanics and special relativity.

## Contents

- `Lectures/`: LaTeX source for Lectures 1--15
- `Lecture_1.pdf`--`Lecture_15.pdf`: compiled lecture notes
- `Course_Schedule.tex` and `Course_Schedule.pdf`: course schedule
- `Figures/` and the PDF figures in the repository root: assets required to compile the notes

To compile a lecture from the repository root, run, for example:

```bash
latexmk -pdf Lectures/Lecture_4.tex
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

When new lecture material or corrections are published:

1. Open your fork on GitHub.
2. Switch to its `main` branch.
3. Click **Sync fork** and then **Update branch**.
4. Merge the updated `main` branch into your `my-notes` branch.

The final merge can be performed in a local Git checkout. Replace `YOUR-USERNAME` with your GitHub username:

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

If your changes and an official update modify the same lines, Git will report a merge conflict. You must choose which version to keep, finish the merge, and push the result to your fork. See GitHub's instructions for [synchronizing a fork](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork).

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

This public repository is generated from a separately maintained private course repository. Official changes are made in the private source repository and published here automatically after a successful LaTeX build.

## Licence

Except where otherwise noted, these lecture materials are copyright Daan Meerburg and licensed under the [Creative Commons Attribution 4.0 International licence](https://creativecommons.org/licenses/by/4.0/).

Third-party material is not covered by this licence unless explicitly indicated. Such material remains subject to its original copyright and licence terms.
