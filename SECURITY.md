# Security Policy

## Reporting a vulnerability

Do not open a public issue for a suspected vulnerability. Use GitHub private
vulnerability reporting for this repository.

Provide the minimum evidence needed to reproduce the issue. Never include real
participant private keys, seed phrases, production credentials, unredacted
identity records, or live transaction secrets.

## Security-sensitive scope

The following areas require explicit security review before release:

- funding, release, refund, dispute, freeze, unfreeze, and recovery paths;
- privileged roles, role transfer, multisignature, and timelock behavior;
- attestation domains, quorum, signer authorization, nonce, and expiry;
- token, chain, recipient, amount, and contract-address validation;
- factories, registries, deployment manifests, and code hashes;
- events relied upon by indexers and reconciliation;
- SDK signing, webhook verification, idempotency, and replay protection.

## Production status

Source code is not evidence of an official production deployment. An official
deployment requires a reviewed manifest under `deployments/` that binds the
chain ID, address, code hash, protocol version, constructor arguments, approved
asset, audit status, and governance authority.
