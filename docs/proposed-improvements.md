# Proposed improvements

Suggestions received from readers, what the prompt does today, and the change
each one would lead to. Nothing on this page is implemented yet.

Every change to `prompts/project_ideation.md` must be mirrored in
`skills/idea-to-launch/SKILL.md` and `prompts/project_ideation.compact.md`.

## 1. Separate verified findings from guesses

Received on 2026-10-14, in a comment on the launch post.

**Suggestion.** In the competitor step, give a source link for each
competitor, and mark domain availability "not checked" unless it was actually
checked. Otherwise a polished launch plan can make an untested idea feel
validated. The comment also asked whether the prompt pauses for evidence
before choosing which idea to pursue.

**What the prompt does today.**

- Rule 3 (*Evidence over opinion*) asks for sources and says to label
  anything that cannot be verified as an assumption. It sets no format, so a
  model without web search can produce output that reads as more checked than
  it is.
- Phase 4 is a gate. Every option is scored on feasibility, originality,
  effort against result and existing competition, with a quick web search for
  the competition. The model then recommends one, and the session stops until
  the user chooses. It pauses for a decision, not for a minimum amount of
  evidence.
- The deep competitor research (3–7 named examples with links) is in
  Phase 6, after the choice. Phase 6 may conclude that the space is saturated,
  and rule 5 lets the user go back and pick another option.
- Phase 7 says to verify name and domain availability rather than guess, but
  not what to write when the check could not be done.

**Proposed changes.**

- Phase 4 and Phase 6: each competitor carries a source link, or "not
  verified" when there is none.
- Phase 4: the comparison table says which scores rest on evidence found in
  the session and which rest on assumptions. If the competition column has no
  sources, the model says so before asking the user to choose.
- Phase 7: each availability check (domain, handles, trademark, existing
  companies and products) is marked "checked", with its source, or "not
  checked". Without web search every check is "not checked", and the model
  says so.
- Closing: the final recap lists the assumptions that are still unverified,
  so the plan does not read as validation of the idea.

## 2. A sample run where an idea is rejected

Received on 2026-10-14, in the same comment.

**Suggestion.** Publish a sample run in which an idea is rejected on
evidence, to show how the selection works.

**Today.** The repository has no sample run: neither the README nor
[USAGE.md](USAGE.md) shows one.

**Proposed change.** Add a trimmed transcript of a real session under
`docs/examples/`, in which a candidate idea is dropped in Phase 4 or Phase 6
on evidence, with the sources that decided it. Link it from the README.
