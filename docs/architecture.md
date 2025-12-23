# Ember Tideledger — Architecture Overview

This document provides a high-level overview of the project structure,
Base alignment, and key design decisions.

---

## Project Structure

- `config/`  
  Static configuration files (networks, environments).

- `docs/`  
  Internal documentation for maintainers and reviewers.

- `scripts/`  
  Helper inputs and utilities used during validation and testing.

---

## Base Alignment

Ember Tideledger is **Base-first** by design:

- Supports Base Mainnet and Base Sepolia only
- Uses official public Base RPC endpoints
- Explorer links target BaseScan domains
- Network metadata is centralized in config (no hardcoded values)

---

## Design Decisions

### Static Configuration
All network-related data lives in JSON files to:
- Avoid duplication in code
- Make reviews and audits simpler
- Enable safe future expansion

### Read-Only First
Validation and probing prioritize:
- Read-only balance checks
- Block and metadata inspection
- No assumptions about wallet type (EOA vs smart account)

### Minimal Surface Area
- Fewer dependencies
- Clear separation between config, docs, and logic
- Explicit defaults

---

## Future Considerations

- Optional env-based RPC overrides
- JSON Schema validation in CI
- Additional Base test networks if introduced

_Last updated: initial scaffold_
