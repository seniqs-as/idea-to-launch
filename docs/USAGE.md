# Using idea-to-launch on any platform

The content is plain Markdown, so it works with any capable AI assistant. Pick the file that fits your platform.

| File | Size | Best for |
|------|------|----------|
| [`prompts/project_ideation.md`](../prompts/project_ideation.md) | ~8.4k chars | Full version: first message, Projects, API system prompt, agent tools |
| [`prompts/project_ideation.compact.md`](../prompts/project_ideation.compact.md) | ~4.1k chars | Anything with a character limit (Custom GPTs, Gems, custom instructions) |
| [`skills/idea-to-launch/SKILL.md`](../skills/idea-to-launch/SKILL.md) | ~8.8k chars | Tools that load skills in the `SKILL.md` format |

## ChatGPT

- **Quick start:** paste the full prompt as your first message in a new chat.
- **Custom GPT (reusable):** *Explore GPTs > Create > Configure*, paste `project_ideation.compact.md` into **Instructions** (limit is 8,000 characters), and enable **Web Search** under Capabilities.
- **Project:** create a Project and paste the full prompt into the project instructions, or upload the file.
- Tip: turn on memory if available, otherwise save the "Session notes" block the assistant produces and paste it into the next session.

## Google Gemini

- **Gem:** *Gems > New Gem*, paste `project_ideation.compact.md` as the instructions.
- Or paste the full prompt as the first message.

## Claude

- **Skill:** see the README (Claude Code folder copy, or zip upload in Claude.ai).
- **Project:** paste the full prompt into the project instructions.

## Skill-based agent tools (Codex CLI, and others)

Tools that follow the `SKILL.md` convention (a folder containing `SKILL.md` with `name` and `description` frontmatter) can use `skills/idea-to-launch/` as is. Copy the folder into the tool's skills directory; check your tool's documentation for the exact path.

## Rules-file based tools (Cursor, Copilot, Windsurf, `AGENTS.md`, ...)

Copy the full prompt (or the compact one) into the tool's rules or instructions file, for example `AGENTS.md`, `.cursor/rules/`, or `.github/copilot-instructions.md`. Strip the YAML frontmatter if you start from `SKILL.md`.

## Any model via API or local runtime

Send `project_ideation.md` as the **system prompt** and have the conversation as normal user turns. Quality depends on:

- **Web search / browsing:** without it the assistant can only label market claims as assumptions, as the prompt instructs.
- **Instruction following:** the "one question at a time" and "converge on one project" rules work best with strong models; small local models may drift.

## Keeping the files in sync

`SKILL.md` and the compact prompt are derived from `project_ideation.md`. If you edit the full prompt, mirror the change in the others.
