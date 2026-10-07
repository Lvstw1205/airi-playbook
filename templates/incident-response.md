# Operational incident response

Record the symptom, affected component, last successful operation and current state. Preserve
durable records. Reconcile transactions before retrying them. Bound retries with backoff and
surface persistent failures. A running process is not proof of successful work.

For a storage error, stop writes to the affected path; never silently create a fresh ledger
where a missing volume should be. For a model error, retain the task and report its status.
For an external side effect with an unknown outcome, query status before resubmission.

After repair, verify a representative operation and document what remains unverified.
Do not claim uptime while the computer is shut down or asleep.
