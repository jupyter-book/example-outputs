---
title: Mulitple Outputs from a Single Cell
short_title: Multiple
kernelspec:
  name: python3
  display_name: Python 3
---

* Matplotlib
* Text
* Markdown
* Image
* HTML


```{code-cell} python3
:label: out-multiple
import matplotlib.pyplot as plt
import numpy as np
from IPython.display import display, TextDisplayObject, Image, HTML, Markdown

img = np.random.random((5,5))

plt.figure(figsize=(3, 3))
plt.xticks([])
plt.yticks([])
plt.imshow(img)
plt.show()

display("Displaying some plain text above the rabbit")

display(Image("./placeholder.jpg"))

display(Markdown("""
# This is Markdown

Albeit a pretty short example of:

* text
* headings
* a list
"""))

display(HTML("""
<div>
   <h1>This is HTML</h1>
   <p>A <strong>strong</strong> paragraph!</p.
</div>
"""))

```

