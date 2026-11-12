# Code Breaking with Statistical Physics
**MATH20014 – Mathematical Programming | University of Bristol | Year 2**

## 1. Project Overview

The aim of this project is to investigate methods for decrypting messages encrypted using substitution ciphers.

Each message uses a permutation of the 27 characters (A–Z and spaces). We will investigate several approaches to recovering the original messages:

1. **Cyclic shifts:** Test all 27 possible shifts to decode the first message.
2. **Frequency analysis:** Compare character frequencies in encrypted messages with those in a sample of English text.
3. **Manual adjustment:** Improve frequency-based guesses by swapping character mappings.
4. **Bigram analysis:** Use frequencies of consecutive character pairs to measure how plausible a decrypted message is.
5. **Metropolis algorithm:** Use a Monte Carlo method to search for increasingly likely decryptions.
6. **Extensions:** Investigate possible improvements, such as simulated annealing, trigrams and analysing algorithm performance.

The final project will include our methods, code, results, decrypted messages and discussion.

## 2. Project Structure

```text
Code Breaking with Statistical Physics/
│
├── main_project.ipynb
│
├── development/
│   ├── frequency_analysis.ipynb
│   ├── bigram_analysis.ipynb
│   ├── metropolis_testing.ipynb
│   └── visualisation.ipynb
│
├── data/
│   └── moby_dick.txt
│
├── .gitignore
└── README.md
```

**`main_project.ipynb`**  
The final, integrated notebook containing the complete project. Keep this organised, readable and suitable for assessment.

**`development/`**  
Separate notebooks for experimenting with individual methods and developing code. These do not need to be polished.

**`data/`**  
Stores external datasets and text corpora used in the project.

## 3. Software and Platforms

We use two main platforms:

| Platform | Purpose |
|---|---|
| Noteable (JupyterLab) | Writing, running and testing Python code in notebooks |
| GitHub | Version control, sharing code and managing contributions |

Our GitHub repository is the central version-controlled copy of the project. Noteable is our working environment.

## 4. Creating a Development Notebook

Each person should develop and test their work in a separate notebook rather than directly editing `main_project.ipynb`.

To create one:

1. Open the project folder in Noteable.
2. Open the `development` folder.
3. Select **New → Notebook** (or the notebook creation option in JupyterLab).
4. Select the Python kernel.
5. Rename the notebook to describe its purpose, e.g. `bigram_analysis.ipynb`.
6. Write and test your code in this notebook.

Once your work is working, the relevant functions and results can be transferred into `main_project.ipynb`.

**Important:** Avoid multiple people editing the same notebook simultaneously. Jupyter notebooks can produce difficult merge conflicts.

## 5. GitHub Collaboration Workflow

Our GitHub repository uses a `main` branch. This should contain the stable, integrated version of the project.

Each person should work on their own branch when making substantial changes.

### Step 1 – Get the latest version

Before starting work, update your local copy:

```bash
git switch main
git pull origin main
```

### Step 2 – Create your own branch

Create a branch named after your task or contribution:

```bash
git switch -c frequency-analysis
```

For example:
- `frequency-analysis`
- `bigram-analysis`
- `metropolis-algorithm`
- `visualisation`

### Step 3 – Save your work

After making changes, open a terminal in the project folder and check:

```bash
git status
```

Stage and commit your changes:

```bash
git add .
git commit -m "Implement frequency analysis"
```

A commit is a saved snapshot of your work, with a description of what changed.

### Step 4 – Push your branch to GitHub

```bash
git push -u origin frequency-analysis
```

For subsequent pushes from the same branch, use:

```bash
git push
```

### Step 5 – Merge your work

Once your work is ready:

1. Open the repository on GitHub.
2. Select **Compare & pull request**.
3. Create a Pull Request from your branch into `main`.
4. Ask another group member to review the changes.
5. Merge the Pull Request once everyone is happy with it.

### Step 6 – Update your local copy

After your work has been merged:

```bash
git switch main
git pull origin main
```

You can then create another branch for your next task.

## 6. Important Collaboration Rules

- Always pull the latest version of `main` before starting new work.
- Work on your own branch rather than directly on `main`.
- Use descriptive commit messages.
- Commit and push regularly rather than waiting until the end.
- Avoid editing the same notebook as another person.
- Do not commit temporary files such as `.ipynb_checkpoints/`.
- Test your code before submitting a Pull Request.
- Review other people's contributions where possible.
- Keep `main_project.ipynb` as the clean, integrated version of the project.

## 7. Quick Git Command Reference

| Command | Purpose |
|---|---|
| `git status` | Check the current state of your files |
| `git switch main` | Switch to the main branch |
| `git pull origin main` | Download the latest changes |
| `git switch -c branch-name` | Create and switch to a new branch |
| `git add .` | Stage your changes |
| `git commit -m "Description"` | Save a commit |
| `git push` | Upload your commits to GitHub |
| `git branch` | List local branches |

**Remember:** Noteable is where we write and run our code. GitHub is where we manage and share our changes.
