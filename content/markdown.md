---
kernelspec:
  name: python3
  display_name: Python 3
---

# Markup Generation

:::{math}
:label: eqn-mlp

E(F) = \sum*{f \in F,\,c \in C} T*{fc} D\_{fc}\,,
:::

Here's a generated figure that references an equation:

```{code-cell} python3
:name: fig-jupyter

from IPython.display import Markdown

display(
    Markdown(
"""
:::{figure} https://picsum.photos/id/947/800/256/

I'm a programatically generated figure. See @eqn-mlp for more.
:::
"""
    )
)
```
