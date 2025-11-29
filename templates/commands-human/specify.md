---
description: Create or update the feature specification from a natural language feature description.
handoffs:
  - label: Build Technical Plan
    agent: speckit.plan
    prompt: Create a plan for the spec. I am building with...
  - label: Clarify Spec Requirements
    agent: speckit.clarify
    prompt: Clarify specification requirements
    send: true
---

## Action Required

You are the human agent. Your task is to create a new feature specification based on the user's input.

### User Input

```text
$ARGUMENTS
```

### Instructions

1.  **Understand the Feature Request:** Read the user's input above to understand what they want to build.

2.  **Determine a Branch Name:**
    *   Come up with a short, descriptive name for the feature (e.g., `user-authentication`, `photo-gallery-drag-and-drop`).
    *   Check for existing local or remote branches with a similar name to determine the next available feature number. For example, if you see `001-user-authentication`, the next number would be `002`.
    *   You can check for existing branches with the following commands:
        *   `git branch -a` (to see all local and remote branches)
        *   `ls specs` (to see existing spec directories)

3.  **Run the `create-new-feature` Script:**
    *   Open a new terminal and run the appropriate script for your operating system. This script will create a new branch and the necessary spec files.
    *   **For Bash (Linux/macOS):**
        ```bash
        scripts/bash/create-new-feature.sh --number <number> --short-name "<branch-name>" --json "<user-input>"
        ```
    *   **For PowerShell (Windows):**
        ```powershell
        scripts\powershell\create-new-feature.ps1 -Number <number> -ShortName "<branch-name>" -Json "<user-input>"
        ```
    *   **Example:**
        ```bash
        scripts/bash/create-new-feature.sh --number 1 --short-name "photo-albums" --json "Build an application that can help me organize my photos in separate photo albums."
        ```

4.  **Create the Specification:**
    *   The script from the previous step will output the path to the newly created `spec.md` file (e.g., `specs/001-photo-albums/spec.md`).
    *   Open this file in your editor.
    *   Fill out the `spec.md` file based on the user's request, following the structure in `templates/spec-template.md`. Be as detailed as possible, including user stories, functional requirements, and success criteria.

5.  **Return to this Terminal:** Once you have created and saved the `spec.md` file, you can return to this terminal and indicate that you have completed the task. You can do this by simply typing "done" or providing a summary of the work you completed.
