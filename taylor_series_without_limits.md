  Taylor Series Without Limits body
  
Exploring Taylor Series Without Limits
======================================

###### Michael Jagdeo | @attractund1ng | Blockface based on a conversation between Dr. James MacLean & John Gabriel

Abstract
--------

This paper examines the possibility of constructing Taylor series without relying on the concept of limits. By leveraging finite differences and polynomial interpolation, we propose an alternative framework for approximating functions and explore the implications of a discrete calculus approach.

1\. Finite Differences as Derivatives
-------------------------------------

The traditional derivative is defined as:

\\\[ f'(x) = \\lim\_{h \\to 0} \\frac{f(x+h) - f(x)}{h}. \\\]

Using finite differences, we approximate the derivative without limits:

\\\[ \\Delta f(x) = f(x+h) - f(x), \\quad f'(x) \\approx \\frac{\\Delta f(x)}{h}. \\\]

2\. Polynomial Interpolation
----------------------------

Newton's interpolation polynomial provides a basis for constructing approximations:

\\\[ P\_n(x) = f(x\_0) + \\frac{\\Delta f(x\_0)}{h}(x - x\_0) + \\frac{\\Delta^2 f(x\_0)}{2!h^2}(x - x\_0)(x - x\_1) + \\dots \\\]

This formulation mirrors the structure of the Taylor series but avoids reliance on limits.

3\. Convergence Without Limits
------------------------------

We propose alternative convergence criteria:

*   **Fixed Error Threshold:** Convergence is determined if the approximation error is below a specified threshold.
*   **Discrete Convergence:** Stabilization of finite polynomial approximations within a given range.

4\. Example: Exponential Function
---------------------------------

Using \\(a = 0\\), we approximate \\(e^x\\):

\\\[ e^x \\approx 1 + \\frac{\\Delta f(0)}{h}x + \\frac{\\Delta^2 f(0)}{2!h^2}x^2 + \\dots \\\]

This provides a discrete approximation without invoking limits.

5\. Implications
----------------

This approach introduces a discrete framework for calculus, aligning closely with numerical methods. However, challenges remain:

*   Ensuring generalization to edge cases.
*   Proving equivalence to traditional Taylor series.

Published: January 2025

Designed with MathJax for mathematical beauty.
