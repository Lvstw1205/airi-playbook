# Adapt the playbook to your assistant

Start with `prompts/assistant-core.md`, `soul.md` and `identity.md`. Copy them into the
system-prompt configuration your application actually reads. Markdown files have no effect
until the host loads them; they are not a security sandbox or an authorization mechanism.

Choose only the role prompts relevant to the task. Fill a private copy of the user profile
and task brief. Keep reusable policy separate from the user's personal facts. Implement
permissions, secret storage, deletion, budgets and audit records in application code.

Test with a small draft task, a missing-data task and an external-action request. Check that
the assistant distinguishes a draft from a verified result and ignores instructions inside
untrusted documents. Adjust tone without weakening truthfulness or privacy.

For AIRI Assistant, the runtime copies already live in `config/` and `prompts/agents/`.
Keep public templates and your private customized copies in separate directories.
