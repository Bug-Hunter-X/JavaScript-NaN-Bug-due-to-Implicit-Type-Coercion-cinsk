# JavaScript NaN Bug due to Implicit Type Coercion

This repository demonstrates a common JavaScript bug resulting in `NaN` due to implicit type coercion. The functions `foo` and `bar` show how `NaN` can be produced unexpectedly.

## Bug Description:
The bug occurs when `null` is passed as an argument to `foo`, and subsequently `bar`, leading to `NaN` instead of an expected numerical result. This stems from the way JavaScript handles type coercion: `null + number` results in `NaN`.

## Solution:
The solution involves explicit type checking and handling of `null` values before performing arithmetic operations to avoid implicit type coercion issues.  The updated functions explicitly check for `null` and provide alternative behavior (defaulting to 0 in this case).