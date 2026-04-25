# Generic Authorization Protocol (GAP) v1.4.1

**`draft-chambers-gap-protocol-01`**

## Status

Internet-Draft — Individual Submission
Intended Status: Standards Track
Author: S. Chambers (Independent)

## Abstract

The Generic Authorization Protocol (GAP) defines a framework for
cryptographically binding, verifying, and enforcing authorization
decisions for autonomous software agents. GAP requires each agent
action to carry a signed authorization envelope containing identity
claims, action descriptors, and cryptographic proof.

## Read the Spec

[Read the Internet-Draft](./draft-chambers-gap-protocol-01.html)

## Key Features

- JWS (RFC 7515) and COSE (RFC 9052) dual signing formats
- Mandatory canonicalization via JCS (RFC 8785)
- 128-bit CSPRNG nonce with replay-window enforcement
- Four-tier assurance levels with downgrade resistance
- Algorithm agility with deprecation lifecycle
- Interoperates with OAuth 2.0, SPIFFE, and X.509

## v1.4.1 Normative Fixes

| Fix | Section |
|-----|---------|
| Mandatory JCS/CBOR canonicalization | Section 4 |
| JWS detached payload with b64:false | Section 5.2 |
| COSE_Sign1 payload rules | Section 5.3 |
| action_params depth/size limits | Section 6 |
| Enumerated assurance_level validation | Section 7 |
| 128-bit nonce plus CSPRNG mandate | Section 8.1 |
| 300s replay window with bounds | Section 8.2 |
| Algorithm registry plus deprecation lifecycle | Section 9 |
| Full signing-scope definition | Section 5.4 |

## References

- [RFC 7515 — JSON Web Signature](https://www.rfc-editor.org/rfc/rfc7515)
- [RFC 8785 — JSON Canonicalization Scheme](https://www.rfc-editor.org/rfc/rfc8785)
- [RFC 9052 — COSE Structures and Process](https://www.rfc-editor.org/rfc/rfc9052)

## License

This document is subject to BCP 78 and the IETF Trust's Legal
Provisions Relating to IETF Documents.
