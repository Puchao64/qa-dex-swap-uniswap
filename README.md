# 🧪 Manual QA Test: Uniswap DEX Swap Interface

This repository contains a structured QA case focused on manual testing of the token swap interface at [Uniswap](https://app.uniswap.org/#/swap). The goal was to validate UI behavior, error handling, and edge cases for swapping tokens without connecting a wallet.

---

## 🎯 Test Objectives

- Ensure proper rendering of the swap interface.
- Validate token selector functionality.
- Confirm correct error responses on invalid or zero amounts.
- Observe UI feedback on hover elements (gas fees, rate).
- Test swap action rejection when wallet is not connected.
- Capture fallback behavior such as swap cancellation (e.g. switching tabs).

---

## 🖼 Screenshots

| Step | Action                                   | Screenshot |
|------|------------------------------------------|------------|
| 1    | Open Uniswap                             | ![homepage](./screenshots/homepage.png) |
| 2    | Select token (e.g. USDC)                 | ![token-select](./screenshots/token-select.png) |
| 3    | Enter amount                             | ![amount-input](./screenshots/amount-input.png) |
| 4    | Enter invalid amount (`0.000...01`)      | ![invalid-amount](./screenshots/invalid-amount.png) |
| 5    | Attempt swap without wallet              | ![no-wallet-error](./screenshots/no-wallet-error.png) |
| 6    | Hover over gas info / rate               | ![gas-info-hover](./screenshots/gas-info-hover.png) |
| 7    | Cancel or exit swap (via Limit tab)      | ![cancel-swap](./screenshots/cancel-swap.png) |

---

## ⚙️ Environment

- **Browser**: Chrome
- **Network**: Mainnet (Uniswap default)
- **Wallets**: Not connected (intended)
- **Language**: English UI
- **Tools**: Manual screenshots, mouse-based interaction

---

## ✅ Result

All UI behaviors function as expected for a disconnected user.  
Errors are triggered properly for invalid input, hover tooltips display contextual help, and the interface prevents unauthorized swaps.

Uniswap's DEX frontend demonstrates a robust and intuitive UI that handles edge cases gracefully.
