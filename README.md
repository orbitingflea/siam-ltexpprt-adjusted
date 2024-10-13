# Adjusted LaTeX Template for SIAM Preprint/Proceedings

## Introduction

`ltexpprt.sty` is a template that is mainly used for SIAM conference papers such as SODA and SOSA. However, it defines the proof and theorem environments in a non-standard way, which conflicts with the commonly used package `amsthm`. This repository is a slighly adjusted version that replaces the proof and theorem environments with the `amsthm` implementation, while the visual effects are almost the same as the initial template.

Files in this repository:
- `ltexpprt.sty`: the adjusted template.
- `ltexpprt.original.sty`: the original template. Before using the adjusted version, make sure that the original template is the same as yours, i.e., `ACM/SIAM LaTeX2E Preprint Series macro package, version 1.2.1, November 27, 2023`.
- `ltexpprt_singlecolumn.pdf` and `ltexpprt_singlecolumn.original.pdf`: sample pdf files by compiling the provided sample tex file with the adjusted and original versions of the template, respectively. This is only for comparison.

This repository is mainly for personal use and is not guaranteed to work in any scenario. Use at your own risk.

## Features

1. Theorems, lemmas and other environments are defined using the `amsthm` package. Some of them are naturally supported by `cleveref`.
2. For proofs, one can customize the heading text:
   ```latex
   \begin{proof}[Proof of Theorem 1]
     Theorem 1 is true because
     \[ 1+1=2. \qedhere \]
   \end{proof}
   ```
3. `\qedhere` when a proof ends with a formula. See the above example.
