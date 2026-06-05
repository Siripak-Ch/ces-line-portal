# Frontend Audit — Backend Confirmed OK

Scope: frontend GitHub only. Backend Apps Script is treated as correct and unchanged.

## Checked

- `js/config.js` contains expected sheet IDs for Main / KPI / Stock.
- `js/gas-polyfill.js` supports GitHub Pages calls to Apps Script Web App.
- `api-test-all.html` includes tests for Core, Read Modules, KPI, Stock Dashboard, Inventory, and Check Stock.

## Sheet IDs

```text
MAIN  = 1w3_j_2T67f9xy_ndGYw9LuuKCPEttw52zwVUxM1zUNE
KPI   = 1vNt7qUenxteIV3A0TnQ2QYf0esyOu3NvEjZG8zme5Gk
STOCK = 1X7f6BatQ-y5ZW6VYTv2oT34rbsCLeNgac0APt7njFrk
```

## Verification after upload

Open:

```text
https://siripak-ch.github.io/ces-line-portal/api-test-all.html
```

Run:

```text
Run Core
Run Read Modules
Run Stock
```

If tests fail with `Function not allowed or not found`, backend allow list/deployment must be checked; frontend is already calling the expected public function names.
