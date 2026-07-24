---
name: Withdraw funds from BitOasis
description: Check balances, then withdraw crypto to an external address or fiat to a registered bank, and track the withdrawal.
api: openapi/bitoasis-exchange-openapi.yml
operations: [getBalances, getBanks, getCoinWithdrawalFees, newCoinWithdrawal, getCoinWithdrawal, newFiatWithdrawal, getFiatWithdrawal, cancelFiatWithdrawal]
---

# Withdraw funds from BitOasis

Move crypto or fiat out of a BitOasis account via the Exchange API
(`https://api.bitoasis.net/v1`). Withdrawals are high-consequence and irreversible
(crypto) or bank-bound (fiat) — always confirm with the user before executing.
Requires a Bearer API token with the relevant withdrawal write permission.

## Steps

1. **Check balances.** Call `getBalances` to confirm sufficient funds in the target
   currency.
2. **Crypto withdrawal:**
   - Call `getCoinWithdrawalFees` to read the per-currency fee.
   - Call `newCoinWithdrawal` with `currency`, `amount`, `withdrawal_address` (and
     optional `network` / `withdrawal_address_id`). This is an irreversible on-chain
     transfer — confirm the address and network first.
   - Track with `getCoinWithdrawal` (by `withdrawal_id`) or list via
     `getCoinWithdrawals` for the currency.
3. **Fiat withdrawal:**
   - Call `getBanks` to pick a registered bank account.
   - Call `newFiatWithdrawal` with `amount` as `{ value, currency }` (and optional
     `origin`).
   - Track with `getFiatWithdrawal`; cancel a pending one with
     `cancelFiatWithdrawal` (`DELETE` by `withdrawal_id`).

## Rules

- No idempotency key exists — do not retry a withdrawal on timeout; reconcile via
  the list/get operations first to avoid double-withdrawing.
- 401 means the token lacks withdrawal permission; 400 means an invalid
  address/amount/bank. See `errors/bitoasis-problem-types.yml`.
- Treat every withdrawal as safety-critical: require explicit human confirmation.
