<p align="center">
  <img src="assets/i-t-l.png" alt="idea-to-launch: a light bulb launching like a rocket" width="480">
</p>


# idea-to-launch

**A structured AI interview that takes you from vague interests to one validated, feasible project.**

`idea-to-launch` is a prompt (and a ready-to-install Claude skill) that turns an AI assistant into a project ideation partner: part interviewer, part strategist, part critical reviewer. It does not dump a list of ideas. It asks questions one at a time, narrows the field with an explicit scoring comparison, and then stress-tests the winning idea against the real market, with cited sources.

## Why this exists

With modern AI, the hard part of building something is no longer the building. Code, copy, designs and prototypes that once took weeks, a team or a budget can now be produced in hours by one person with an assistant.

The bottleneck has moved upstream. The scarce skills are now:

1. **Finding ideas worth pursuing**: ones that fit your real skills, time and budget, and that have room in an actual market.
2. **Planning the path from idea to launch**: defining who it is for, what the minimum version is, how it differs from what already exists, and how to bring it to people.

Most people can now execute faster than they can decide *what* to execute. A weak idea built quickly is still a weak idea, and a good idea without a plan stalls just the same.

`idea-to-launch` was created to close that gap. Instead of generating a pile of generic ideas, it interviews you, challenges your assumptions with evidence, narrows everything down to one project, and leaves you with a validated definition and a concrete plan, ready to hand to the same AI that will help you build it.

## What it does

The session moves through eight phases, with a short recap and confirmation at the end of each:

| # | Phase | Outcome |
|---|-------|---------|
| 1 | Context | Individual or company? What does the assistant already know about you? |
| 2 | Project categories | Open the field: web app, physical product, content, service business, non-profit... |
| 3 | Explore and connect | Interests, goals, time, budget, skills, assets, risk tolerance |
| 4 | Comparison and convergence | Options scored on feasibility, originality, effort-to-payoff and competition. You pick **one** |
| 5 | Definition | Target user, problem, why now, MVP, success criteria, what you will *not* build |
| 6 | Competitive landscape | 3-7 real, named competitors with links, pricing and differentiation angles |
| 7 | Name and domain | Availability checks: trademarks, domains, social handles (optional) |
| 8 | Market analysis and marketing plan | TAM/SAM/SOM, personas, risks, positioning, channels, 30/60/90-day plan (optional) |

## Principles

- **Interview, don't lecture.** One question at a time.
- **First-principles thinking.** Assumptions are stated and challenged.
- **Evidence over opinion.** Market claims are backed by sources; anything unverified is labelled as an assumption.
- **You drive.** The assistant clarifies what you want, it does not push its own preferences.
- **Honest, not agreeable.** Weak ideas and saturated markets are called out directly.
- **Backtracking is always allowed.** Change your mind at any point without losing context.

## Repository layout

```
prompts/project_ideation.md          Full prompt, works with any AI assistant
prompts/project_ideation.compact.md  Shorter version for character-limited fields
skills/idea-to-launch/SKILL.md       Same content packaged as a skill (SKILL.md format)
docs/USAGE.md                        Per-platform setup guide
LICENSE                              MIT
```

## Usage

Works with Claude, ChatGPT, Gemini, and any assistant that accepts a system prompt or instructions. For best results use a model with web search enabled, since the prompt asks for cited, real-time market evidence.

| Platform | How |
|----------|-----|
| Any chat | Paste [`prompts/project_ideation.md`](prompts/project_ideation.md) as the first message |
| ChatGPT Custom GPT / Gemini Gem | Paste [`prompts/project_ideation.compact.md`](prompts/project_ideation.compact.md) into the instructions field |
| Claude Code | `cp -r skills/idea-to-launch ~/.claude/skills/` (or `.claude/skills/` per project), then ask *"Help me find a project to build"* or run `/idea-to-launch` |
| Claude.ai | Zip the `idea-to-launch` folder and upload it under *Settings > Capabilities > Skills* |
| Skill-based agent tools | Copy `skills/idea-to-launch/` into the tool's skills directory |
| API / local models | Use the full prompt as the system prompt |

Step-by-step instructions for each platform are in [`docs/USAGE.md`](docs/USAGE.md).

## Tips

- Enable web search / browsing so competitor, pricing and domain checks are real.
- Enable memory if your assistant supports it: the prompt records constraints, decisions and discarded options.
- The session runs in the language you write in; ask to switch at any time.

## Author

Created by **Seniqs AS** - [seniqs.no](https://seniqs.no).

## License

Released under the [MIT License](LICENSE). Use it, adapt it, and build on it freely.
