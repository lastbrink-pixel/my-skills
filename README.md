# my-skills

Personal collection of [Agent Skills](https://agentskills.io) — portable instruction packages for AI coding agents (Claude Code, Copilot agent mode, Codex, Cline, and 70+ others). One repo as the single source of truth, installable on any machine.

## Install (any machine)

```bash
# first install
npx -y skills add lastbrink-pixel/my-skills -g -y

# pull updates later
npx skills update
```

The `-g` flag installs to `~/.agents/skills` (user-level), and the CLI symlinks skills into every supported agent automatically.

## Structure

```
skills/
  find-skills/       # discover & install skills from the marketplace via `npx skills`
    SKILL.md
```

Each skill is a folder under `skills/` containing a `SKILL.md` with YAML frontmatter (`name`, `description`) followed by instructions. Optional supporting files (scripts, templates, references) live alongside it.

## Adding a new skill

```powershell
mkdir skills\my-new-skill
# create skills\my-new-skill\SKILL.md, then:
git add . ; git commit -m "Add my-new-skill" ; git push
```

## Using skills in claude.ai

Skills from this repo can also be used in Claude chats (web/desktop/mobile): zip the skill folder (folder itself as the archive root) and upload it in **Customize → Skills**. Uploaded skills are account-level and available on all devices.

```powershell
Compress-Archive -Path "skills\find-skills" -DestinationPath "find-skills.zip" -Force
```

## Skills

| Skill | Description |
|---|---|
| `find-skills` | Helps discover, search and install agent skills from the open ecosystem ([skills.sh](https://skills.sh)) via the `npx skills` CLI. Source: [vercel-labs/skills](https://github.com/vercel-labs/skills). |
