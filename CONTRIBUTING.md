# Contributing

All changes must be proposed through a pull request. Direct changes to `main`
are not part of the intended workflow.

Every pull request must state:

- the problem and bounded change;
- whether financial state, authority, custody, or tenant isolation is affected;
- compatibility impact on contracts, SDKs, schemas, events, and deployments;
- the exact tests performed, including negative and replay cases where relevant;
- whether independent security review is required.

Protocol behavior must be specified before implementation. A change that
weakens an invariant, mutates an activated settlement template, or changes the
rules governing already-funded settlements requires an explicit architecture
decision and may require a new immutable protocol version.
