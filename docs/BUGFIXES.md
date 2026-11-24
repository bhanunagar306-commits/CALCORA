# Bug fixes in this build

1. Scientific functions now auto-close missing parentheses when `=` is pressed.
2. Animation preference shows a clear ON/OFF indicator.
3. Sign toggle handles unary negative numbers and subtraction operands more consistently.
4. Number-base conversion validates integer text before using `BigInt`.
5. Domain errors have clearer user-facing messages.

Suggested regression sequences:
- Scientific: `√` → `1` → `4` → `4` → `=` → `12`
- Scientific: `∛` → `−` → `8` → `=` → `−2`
- Scientific DEG: `sin` → `3` → `0` → `=` → `0.5`
- Basic: `5` → `+` → `−` → `8` → `=` → `−3`
- Basic: `8` → `±` → `=` → `−8`
