# Cotsel

Cotsel is programmable settlement infrastructure for institutional digital asset transactions. It enables organizations to escrow assets, release funds against verified commercial evidence, enforce policy and multi-party approvals, and reconcile settlement end to end.
## Repository structure

```text
Cotsel/
├── contracts/
│   ├── protocol/             Settlement contracts and state machine
│   ├── factory/              Tenant contract deployment factory
│   ├── registry/             Protocol version and deployment registry
│   ├── interfaces/           Public contract interfaces
│   ├── deployment/           Contract deployment tooling
│   └── tests/                Unit, fuzz, and invariant tests
│
├── packages/
│   ├── sdk/                  Customer-facing Cotsel SDK
│   ├── webhook-verifier/     Webhook signature and replay verification
│   ├── event-schemas/        Versioned public event schemas
│   └── contract-types/       ABI-generated contract types
│
├── specification/            Protocol rules, state machine, and invariants
├── deployments/              Verified addresses, versions, and code hashes
├── examples/                 Neutral customer integration examples
└── docs/                     Public architecture and integration documentation
```

The private API, dashboard, backend services, workers, tenant data, provider
connections, and infrastructure are maintained separately in
`Cotsel/Cotsel-platform`.
