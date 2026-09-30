# Repository Operations and Inventory

This guidance applies to `hpc-isr` repositories listed in the [repository inventory](https://github.com/hpc-isr/hpc-internal-orchestration/blob/main/inventory/repositories.yaml), and to any additional repository explicitly brought into scope. The inventory is a working, evidence-backed register, not proof that every organization repository is listed.

## Before work

- Read this guidance, the repository's own `AGENTS.md`, `README.md`, and task-relevant instructions before acting. Repository-specific requirements remain authoritative for that repository; resolve conflicts explicitly instead of silently overriding them.
- Audit every in-scope repository before making changes. Check the local root, branch/upstream, working tree, recent history, relevant files, and the task-relevant GitHub state. For a requested full audit, cover structure, architecture, code, security, dependencies, validation, documentation, automation, releases, and GitHub metadata. State which repositories and areas were checked and which could not be checked.
- Treat local files, hosted metadata, and user-provided information as separate evidence sources. Verify time-sensitive claims against their strongest available source. Mark facts, assumptions, estimates, unknowns, and contradictions clearly; cite evidence and verification dates where useful.

## Record project knowledge

- Store durable, useful project information in the repository that owns it, using its established files and formats. Update authoritative records instead of creating parallel copies. Keep cross-repository relationships as links or identifiers, not duplicated source content.
- Preserve provenance, current status, ownership, dates, dependencies, and change history when they are relevant and supported. Never invent values or silently resolve conflicting evidence.
- Do not commit credentials, secrets, private personal data, or restricted operational details. Keep sensitive information in its approved system and record only a safe reference when needed.
- Improve these rules when repeated work exposes a real gap. Make the smallest coherent change to the canonical guidance, check for conflicting copies or links, and preserve unresolved decisions as unresolved.

## Branches and delivery

- Prefer working directly on the repository's `main` branch when it is clean, current, and permitted by repository instructions, branch protections, access controls, and concurrent work. If direct work is unsafe or blocked, use the repository's approved branch and review process; do not bypass protections to satisfy the preference for `main`.
- Preserve unrelated or concurrent changes. Never reset, force-push, or discard work to make a task easier. Before publishing a justified change, inspect the working tree and complete diff, stage with `git add --all`, review the staged diff, commit with an appropriate action tag such as `[ADD]`, `[UPDATE]`, `[FIX]`, `[REMOVE]`, or `[REFACTOR]`, fetch and rebase on the appropriate upstream, then push. Stop and report conflicts or policy blockers that cannot be resolved safely.
- Re-read changed files, Git state, and any affected hosted state after publication. Do not claim a change reached `main` until the remote state confirms it.

## GitHub coordination

- Treat Issues, Pull Requests, Discussions, Milestones, Projects, labels, reviewers, assignees, and relationships as part of the maintained project state. When repository work changes, check for relevant metadata drift; when metadata changes, check for needed documentation or code updates.
- Update existing artifacts where possible. Use Issues for actionable work, Pull Requests for reviewable repository changes, and Discussions for genuine open questions or early coordination. Avoid duplicates and unnecessary artifacts.
- Keep artifact titles broad and durable. Use existing labels consistently; Issues should normally have one type, one priority, and one status label. Label every Pull Request, assign a clear owner, and request review when independent review is needed. Keep fields, links, acceptance criteria, validation evidence, blockers, and remaining work synchronized when applicable.
- Add comments only when they contribute new information: what was checked, changed, verified, what remains unresolved, and the next action. Link relevant evidence and use a person's GitHub handle when known. Close work only when its scope is complete and verified, or when it is demonstrably obsolete, duplicated, or superseded.

## Reporting

Report concise findings with evidence, severity or operational impact where relevant, work performed, validation, remaining uncertainty, blockers, and the smallest useful next step. Distinguish completed local work, pushed changes, open review, merged changes, and manually required actions. Do not claim unverified checks or completion.
