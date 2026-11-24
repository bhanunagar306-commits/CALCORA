# CALCORA QA results — follow-up bug-fix build

## Confirmed issues found in the previous build
- Scientific function keys inserted an opening parenthesis but calculation did not close it automatically. This made the normal key sequence `√`, `144`, `=` fail even though `sqrt(144)` itself evaluated correctly.
- The animation preference had no visible ON/OFF state, making its effect unclear.
- Sign-toggle handling did not reliably distinguish a unary minus from a subtraction operator.
- Number-base input accepted some decimal-looking strings through numeric coercion before passing them to `BigInt`.

## Fixes in this build
- Calculation now closes unmatched opening parentheses before evaluation. This supports direct key sequences such as `√ 144 =`, `∛ − 8 =`, and `sin 30 =`.
- The animation setting now displays an explicit ON/OFF status and updates immediately when changed. OFF disables CSS animations and transitions.
- Sign toggle now handles negative values and negative operands more consistently.
- Number-base input now requires a whole-number string before conversion to `BigInt`.
- Function-domain errors now show a more useful message.

## Automated checks completed for this build
- JavaScript syntax check: passed (`node --check`).
- HTML ID references used by JavaScript: all present.
- Duplicate HTML IDs: none found.
- Service-worker precache paths: all referenced local files exist.
- ZIP integrity: checked after packaging.
- Evaluator checks: passed for square root, negative cube root, operator precedence, parentheses, contextual percentages, DEG trigonometry, inverse trigonometry, and exponent associativity.

## Still requires manual testing
- Full browser interaction and visual regression testing on Windows, Android and iOS.
- Keyboard-only and screen-reader accessibility testing.
- PWA install and offline testing on an HTTPS deployment.
- Actual Microsoft Store package validation and certification.

## Test limitation
The browser automation runtime in this environment blocked local browser navigation, so this report does not claim full end-to-end browser testing. The source-level, parser-level and file-integrity checks above were completed.
