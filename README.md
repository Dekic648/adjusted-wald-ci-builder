# Adjusted-Wald Confidence Interval Builder

An interactive calculator for computing confidence intervals around task completion rates in UX research.

**[Try it live →](https://dekic648.github.io/adjusted-wald-ci-builder/)**

## What it does

Enter task results (successes out of total attempts) and get properly computed confidence intervals using the **Adjusted-Wald method**, which outperforms the standard Wald formula at sample sizes common in UX research (n < 40).

The tool:
- Computes **Adjusted-Wald CIs** with automatic LaPlace correction for 0% and 100% outcomes
- Side-by-side comparison with **standard Wald** to show why the traditional method is flawed at small n
- Supports multiple tasks, configurable confidence levels (90%, 95%, 99%)
- Visual interval bars for quick comparison

## Method

| Component | Source |
|---|---|
| **Adjusted-Wald CI** | Agresti, A. & Coull, B. (1998). Adds z²/2 pseudo-successes and z²/2 pseudo-failures before computing. |
| **LaPlace correction** | Used for 0% or 100% outcomes where standard formulas collapse. |
| **Recommendation** | Sauro, J. & Lewis, J.R. (2016). *Quantifying the User Experience* (2nd ed.). |

## Why not standard Wald?

The standard formula `p ± z·√(p(1-p)/n)` produces intervals that are too narrow and can fall outside [0, 1] at small n. Adjusted-Wald consistently outperforms it.

## License

MIT
