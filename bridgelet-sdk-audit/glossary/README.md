# Bridgelet SDK Glossary

This directory contains definitions and conceptual overviews for key terminology and architecture decisions within the Bridgelet SDK.

## Account-Creation Terms

- [Authorized Controller (SDK Side)](./authorized-controller-sdk-side.md): Explains how account creation sets the on-chain `authorized_controller` value.
- [Two-Phase Account Creation](./two-phase-account-creation.md): Describes the SDK's separation of account creation and later payment confirmation.
- [Pending Payment vs Pending Claim](./pending-payment-vs-pending-claim.md): Defines the database states used between account funding and claim completion.
- [Claim Lifecycle](./claim-lifecycle.md): Defines the states and transitions tracked by the claims module.
- [Expiry Ledger Conversion](./expiry-ledger-conversion.md): Explains conversion between wall-clock expiry times and Stellar ledger sequences.
- [Instance Storage TTL](./instance-storage-ttl.md): Describes how Soroban instance storage time-to-live affects account data.

## RPC And Infrastructure Terms

- [Asset Address Resolution](./asset-address-resolution.md): Describes how configured asset identifiers become Stellar contract addresses.
- [Horizon vs Soroban RPC](./horizon-vs-soroban-rpc.md): Distinguishes the Horizon and Soroban RPC APIs used by the SDK.
- [Transaction Polling](./transaction-polling.md): Describes the poll-until-confirmed behavior of `waitForTransaction()`.
- [Error String Matching](./error-string-matching.md): Explains how contract error strings are mapped into SDK errors.
- [i128 / BigInt Encoding](./i128-bigint-encoding.md): Documents the encoding of large signed contract integers.
- [ScVal Map Parsing](./scval-map-parsing.md): Explains manual parsing of maps returned as Soroban `ScVal` values.
- [Stroop Amount Parsing](./stroop-amount-parsing.md): Defines conversion between Stellar stroops and human-readable amounts.
- [Integrator API Keys](./integrator-api-keys.md): Describes integrator authentication and API-key handling.

## Payment, Sweep And Webhook Terms

- [Payment Monitor Polling Interval](./payment-monitor-polling-interval.md): Documents how often pending accounts are checked for payments.
- [Sweep Nonce (SDK Side)](./sweep-nonce-sdk-side.md): Explains how the SDK obtains and uses the on-chain sweep nonce.
- [Webhook Event Types](./webhook-event-types.md): Lists the event names available to webhook subscribers.

These entries serve as a knowledge base for internal audits and onboarding; add new entries to the appropriate thematic section.
