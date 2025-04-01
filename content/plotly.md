---
kernelspec:
  name: python3
  display_name: Python 3
---

# Plotly

```{code-cell} python3
import plotly.graph_objects as go
import numpy as np

np.random.seed(1)
```

```{code-cell} python3
#| label: fig-plotly

# Number of data points
N = 10000

# Generate random data
x = np.random.randn(N)
y = np.random.randn(N).astype('float32')
z = np.random.randint(size=N, low=0, high=256, dtype='uint8')
c = np.random.randint(size=N, low=-10, high=10, dtype='int8')

fig = go.Figure(data=[go.Scatter3d(
    x=x,
    y=y,
    z=z,
    marker=dict(color=c),
    mode='markers',
    opacity=0.2
)])

fig.show()
```
