# test-cldpm

This is a CLDPM-managed mono repo for Claude Code projects.

## Structure

- `shared/` - Shared components (skills, agents, hooks, rules)
- `projects/` - Individual projects

## Quick Start - EXECUTE THESE COMMANDS

```bash
# Create a new project
cldpm create project my-project -d "My awesome project"

# Create shared components
cldpm create skill my-skill -d "Reusable skill"
cldpm create agent my-agent -d "Shared agent"

# Add components to project
cldpm add skill:my-skill --to my-project

# View project info
cldpm get my-project

# After git clone, restore symlinks
cldpm sync --all
```

<!-- CLDPM-SECTION-START -->
## CLDPM Commands - EXECUTE THESE

This project uses CLDPM. **Run these commands** for project management:

```bash
# Creating
cldpm create project <name>         # Run for: "create project"
cldpm create skill <name>           # Run for: "create skill"

# Managing
cldpm add skill:<name> --to <proj>  # Run for: "add skill to project"
cldpm remove skill:<name> --from <proj>  # Run for: "remove skill"

# Viewing
cldpm get <project>                 # Run for: "show project", "project info"
cldpm clone <project> <dir>         # Run for: "export project"
cldpm sync --all                    # Run for: "fix symlinks", "after clone"
```

**IMPORTANT**: Always use `cldpm` commands. Never manually edit project.json or create symlinks.
<!-- CLDPM-SECTION-END -->
