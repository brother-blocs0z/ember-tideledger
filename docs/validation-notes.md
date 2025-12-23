# Ember Tideledger — Validation Notes

Step-by-step notes used during **Base Sepolia** testnet validation.

---

## Network Setup

1. Select `base-sepolia` from `config/networks.json`
2. Confirm `chainId` is `84532`
3. Verify RPC connectivity via default endpoint

---

## Read-Only Checks

Run the following checks using sample addresses:

- [ ] Native ETH balance
- [ ] Latest block number
- [ ] Token metadata (symbol / decimals)
- [ ] No write operations attempted

Use values from `scripts/sample-addresses.json` to ensure consistency.

---

## Explorer Verification

For any address or block:
- Ensure links open on `https://sepolia.basescan.org`
- Confirm network context matches Sepolia
- Avoid mixing Mainnet and Testnet explorers

---

## Failure Handling

If validation fails:
- Switch to an RPC fallback
- Re-run read-only probes
- Inspect network config before changing code

---

## Final Gate

Before merging:
- [ ] All checks pass on Base Sepolia
- [ ] No config drift detected
- [ ] Docs updated if behavior changed

_Last updated: initial scaffold_
