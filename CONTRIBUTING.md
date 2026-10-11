# Contributing to idea-to-launch

Thanks for wanting to improve this. The project is three Markdown files and a usage guide: there is no code, no build and no test suite, so contributing is mostly about how the prompt behaves in a real session.

## What helps most

- **Reports of the prompt misbehaving.** The assistant asks ten questions at once, skips the comparison in Phase 4, never converges on one project, presents unverified market claims as facts, and so on.
- **Wording changes that fix such a behaviour**, ideally with the session that showed the problem.
- **Platform instructions** in `docs/USAGE.md`: a platform that is missing, or steps that no longer match the product.
- Typos and broken links.

## Reporting a problem

Open an issue and include:

- the assistant and model you used, and how you loaded the prompt: first message, custom instructions, project instructions or skill
- which file you used: the full prompt, the compact prompt or `SKILL.md`
- whether web search was enabled
- what the assistant did and what you expected, with the relevant excerpt of the conversation

A session is about your own plans, money and skills. Remove anything personal or confidential before pasting it: issues are public.

## Changing the prompt

`prompts/project_ideation.md` is the source. The other two files are derived from it:

- `prompts/project_ideation.compact.md` is the same interview compressed for fields with a character limit. Keep it well under 8,000 characters, the limit of a Custom GPT's instructions.
- `skills/idea-to-launch/SKILL.md` is the full prompt packaged as a skill, with YAML frontmatter (`name`, `description`). Keep the frontmatter valid: tools use it to decide when to load the skill.

A change to the rules or the phases goes into all three files in the same pull request. If the size of a file changes noticeably, update the table at the top of `docs/USAGE.md`.

There is no automated test. Before opening a pull request, run at least the first phases of a session with your version, and say in the description which assistant and model you used and what changed in its behaviour.

## What is unlikely to be merged

The principles in the README are the point of the project: one question at a time, convergence on one project, evidence over opinion, honesty over agreeableness. A change that trades one of them away (a prompt that returns twenty ideas, or one that drops the cited sources) belongs in a fork, which the MIT license allows.

The files stay in English. The prompt already tells the assistant to run the session in the user's language, so translated copies are not needed.

For anything larger than a wording fix, such as a new phase, a different scoring model or a new file format, open an issue first so we can agree on the direction before you write it.

## Pull requests

- One change per pull request, with a description of what the assistant does differently.
- Plain Markdown, in English.
- By contributing you agree that your contribution is released under the [MIT License](LICENSE).



