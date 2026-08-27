# Bridgelet SDK Postmortems

These are retrospective knowledge-base writeups, independent of any linked bug-tracking issue. They capture findings, root causes, resolutions, and lessons for future reviews.

## Contract-Consumption Gaps

- [Authorized Controller Correctly Set](./authorized-controller-correctly-set-here.md): Records verification that the SDK passes the intended controller during account creation.
- [Duplicate Asset as Recovery Mechanism](./duplicate-asset-as-recovery-mechanism.md): Documents duplicate-asset behavior used as a recovery path.
- [executeSweep() Error Mapping Gap](./execute-sweep-error-mapping-gap.md): Describes missing or incomplete mapping of sweep contract errors.
- [record_payment Trust Assumption Mismatch](./record-payment-trust-assumption-mismatch.md): Captures the mismatch between SDK assumptions and contract-side payment authorization.
- [Sweep Controller Address Argument Order](./sweep-controller-address-passed-correctly.md): Records verification of the sweep controller contract argument order.
- [Stale Token Transfer MVP Note](./stale-token-transfer-mvp-note.md): Documents an outdated MVP note about token transfer status.
- [Status Field Returned as Raw u32](./status-field-returned-as-raw-u32.md): Describes the contract status value being exposed without higher-level decoding.

## Documentation Drift

- [Accounts Future Auth Scoping Note](./accounts-future-auth-scoping-note.md): Records a future authorization boundary that remains intentionally out of scope.
- [Claim Lifecycle E2E Test Scope](./claim-lifecycle-e2e-test-scope.md): Explains the coverage boundary of claim lifecycle end-to-end tests.
- [ESLint Lint Script Scope](./eslint-lint-script-scope.md): Documents the directories included by the repository lint command.
- [Sweeps README Scope Mismatch](./sweeps-readme-scope.md): Captures where the sweeps documentation previously diverged from implementation scope.

## Resilience Patterns

- [ConfigService getOrThrow Fail-Fast Pattern](./config-getorthrow-fail-fast-pattern.md): Explains why required runtime configuration fails fast when absent.
- [Expire Account Race Window](./expire-account-race-window.md): Describes the check-then-call race window in account expiry.
- [getAccountInfo() Parsing Coupling](./getinfo-parsing-coupling.md): Documents parsing assumptions coupled to the Stellar account-info response shape.
- [Horizon-Soroban Non-Atomicity](./horizon-soroban-non-atomicity.md): Explains the non-atomic boundary between Horizon operations and Soroban calls.
- [Manual i128 Encoding](./i128-encoding-manual-implementation.md): Records the risks of hand-rolled signed integer encoding for contract calls.
- [Overlapping Payment Monitor Ticks](./overlapping-payment-monitor-ticks.md): Describes how concurrent monitor intervals can process the same account.
- [Payment Monitor Single-Asset Limitation](./payment-monitor-single-asset-limitation.md): Documents the monitor's limitation to a single payment asset.
- [Dummy Keypair for Simulation](./sourceaccount-dummy-keypair-for-simulation.md): Explains the dummy source keypair used when simulating transactions.
- [Webhook vs Confirmation Ordering](./webhook-vs-confirmation-ordering.md): Captures ordering considerations between confirmation state and webhook delivery.

## Repository Hygiene

- [No .prettierignore Full-Repository Scan](./no-prettierignore-full-repo-scan.md): Documents the repository-wide formatting check and its implications.
- [Webhook Secret Optional Field](./webhook-secret-optional-field.md): Records the lack of entropy enforcement when webhook secrets are optional.

The template and navigation indexes in this directory support authoring and discovery; they are not postmortem findings.
