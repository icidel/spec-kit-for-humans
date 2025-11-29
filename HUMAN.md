# Human-Driven Agent Instructions

This document outlines the process for a human to act as the "agent" in the Spec-Driven Development workflow. When a command is run, you will be prompted to provide the output that an LLM would typically generate.

## Your Role

Your role is to manually provide the content for the various specification and implementation documents. You will be acting as the "brains" of the operation, while the tooling handles the file creation and organization.

## How it Works

When you run a command like `/speckit.specify` or `/speckit.plan`, the system will prompt you to provide the content for the corresponding file (e.g., `spec.md`, `plan.md`). You will need to provide the content in the format expected by the `spec-kit` tooling.

## Getting Started

1.  **Familiarize yourself with the templates.** The `templates` directory contains the templates for the various documents you will be asked to create. Review these to understand the expected format and content.
2.  **Run the commands.** Start with `/speckit.constitution` and proceed through the workflow as you normally would.
3.  **Provide the content.** When prompted, provide the content for the document. You can use an editor of your choice to prepare the content, and then paste it into the terminal.

## Example

When you run `/speckit.specify`, you will be prompted to provide the content for the `spec.md` file. You should provide content that follows the structure of the `spec-template.md` file, including user stories, functional requirements, and so on.
