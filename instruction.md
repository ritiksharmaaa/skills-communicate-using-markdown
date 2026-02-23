# Project Instructions

_Codebase folder structure and file naming conventions for the **skills-communicate-using-markdown** repository._

---

## Folder Structure

```
skills-communicate-using-markdown/
├── .github/
│   ├── dependabot.yml          # Dependabot auto-update configuration
│   ├── steps/                  # Step-by-step course content (Markdown)
│   │   ├── -step.txt           # Tracks the current active step number
│   │   ├── 0-welcome.md        # Step 0 – Welcome / course intro content
│   │   ├── 1-add-headers.md    # Step 1 – Add Markdown headers
│   │   ├── 2-add-an-image.md   # Step 2 – Embed an image
│   │   ├── 3-add-a-code-example.md  # Step 3 – Add a code block
│   │   ├── 4-make-a-task-list.md    # Step 4 – Create a task list
│   │   ├── 5-merge-your-pull-request.md  # Step 5 – Merge the PR
│   │   └── X-finish.md         # Final step – Course completion content
│   └── workflows/              # GitHub Actions CI/CD workflows (YAML)
│       ├── 0-welcome.yml       # Workflow for step 0 (repo initialisation)
│       ├── 1-add-headers.yml   # Workflow that validates step 1 completion
│       ├── 2-add-an-image.yml  # Workflow that validates step 2 completion
│       ├── 3-add-a-code-example.yml  # Workflow that validates step 3 completion
│       ├── 4-make-a-task-list.yml    # Workflow that validates step 4 completion
│       └── 5-merge-your-pull-request.yml  # Workflow that validates step 5 completion
├── .gitignore                  # Patterns for files Git should ignore
├── LICENSE                     # MIT open-source license
├── README.md                   # Main course landing page shown on GitHub
├── index.md                    # Learner's working Markdown file (edited during the course)
└── instruction.md              # This file – structure & naming convention guide
```

---

## File Naming Conventions

### Root-level files

| File | Convention | Purpose |
|------|-----------|---------|
| `README.md` | `UPPERCASE` with `.md` extension | Standard GitHub repository landing page |
| `LICENSE` | All-caps, no extension | Standard open-source license file |
| `index.md` | `lowercase` with `.md` extension | Primary learner content file |
| `instruction.md` | `lowercase` with `.md` extension | Project documentation / instructions |
| `.gitignore` | Dot-prefixed lowercase | Hidden configuration file for Git |

### `.github/steps/` – Course step files

- **Pattern**: `{step-number}-{kebab-case-description}.md`
- **Examples**: `1-add-headers.md`, `3-add-a-code-example.md`
- **Special files**:
  - `-step.txt` — plain text file containing only the current step number (e.g. `1`)
  - `0-welcome.md` — intro/welcome content displayed before any learner action
  - `X-finish.md` — completion page shown after all steps are done (`X` denotes "finished")

### `.github/workflows/` – GitHub Actions workflow files

- **Pattern**: `{step-number}-{kebab-case-description}.yml`
- **Examples**: `0-welcome.yml`, `4-make-a-task-list.yml`
- Each workflow file corresponds 1-to-1 with a step file in `.github/steps/`.

### `.github/` – Other configuration files

- **Pattern**: `lowercase` with the appropriate extension (e.g. `dependabot.yml`)

---

## Key Conventions Summary

- **Markdown files** use the `.md` extension and `lowercase-kebab-case` names (except `README.md` which follows the GitHub standard).
- **Workflow files** use the `.yml` extension and follow the same `{step-number}-{kebab-case-description}` pattern as their matching step files.
- **Step numbering** starts at `0` (welcome/setup) and increments by `1` for each learner activity. The letter `X` is used for the final completion step.
- **Hidden/config files** are dot-prefixed (e.g. `.gitignore`, `.github/`).
