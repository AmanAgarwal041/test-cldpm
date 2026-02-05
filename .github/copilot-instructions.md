<!-- CLDPM-SECTION-START -->
# CLDPM Mono Repo - GitHub Copilot Instructions

This repository uses **CLDPM (Claude Project Manager)**. When suggesting code or actions, use the `cldpm` CLI.

## EXECUTE These Commands

When the user asks for project management tasks, suggest and execute these commands:

| User Intent | Command to Execute |
|-------------|-------------------|
| Create a new project | `cldpm create project <name> -d "description"` |
| Create a shared skill | `cldpm create skill <name> -d "description"` |
| Create a shared agent | `cldpm create agent <name> -d "description"` |
| Add skill to project | `cldpm add skill:<name> --to <project>` |
| Remove skill from project | `cldpm remove skill:<name> --from <project>` |
| View project structure | `cldpm get <project>` |
| Export standalone project | `cldpm clone <project> <directory>` |
| Restore symlinks | `cldpm sync --all` |

## File Structure

- `cldpm.json` - Root config (DO NOT manually edit)
- `project.json` - Project manifest (managed by cldpm)
- `shared/` - Shared components
- `projects/` - Individual projects

## Installation

**BEFORE running `cldpm` commands**, check if installed and install if needed:

1. **Check**: `which cldpm` or `cldpm --version`
2. **If missing, detect environment and install**:
   - **Python detected** (pyproject.toml, requirements.txt, setup.py, or python/python3 exists): `pip install cldpm` or `pip3 install cldpm`
   - **Node.js/TypeScript detected** (package.json, tsconfig.json, or node/npm exists): `npm install -g cldpm`
   - **Default**: `pip install cldpm` or `pip3 install cldpm`

## Important Rules

1. **Use `cldpm` commands** - don't manually create/edit config files
2. **Run `cldpm sync --all`** after cloning the repository
3. **Use `cldpm add`** to add components - don't manually create symlinks
<!-- CLDPM-SECTION-END -->
