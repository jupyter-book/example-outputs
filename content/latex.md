---
kernelspec:
  name: python3
  display_name: Python 3
---

# LaTeX Generation

Here's a LaTeX equation:

```{code-cell} python3

from IPython.display import Latex

display(
    Latex(
"""
$$
\label{eqn-manual}
E^2 = \left(pc\right)^2 + \left(m_0c^2\right)^2
$$
"""
    )
)
```

And here's a generated LaTeX equation:

```{code-cell} python3
:name: eqn-sympy

from sympy import symbols

x, y = symbols('x y')
z = x**2 + y**2 + 4

display(z)
```

The generated equation in @eqn-sympy is less fancy than that of @eqn-manual!
