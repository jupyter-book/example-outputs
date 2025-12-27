---
kernelspec:
  name: python3
  display_name: Python 3
---

# AST Generation

And a figure

```{code-cell}
display({
  "application/vnd.mystmd.ast+json;version=1": {
  "type": "root",
  "children": [
        {
          "type": "container",
          "kind": "figure",
          "children": [
            {
              "type": "image",
              "url": "https://picsum.photos/id/947/800/256/"
            },
            {
              "type": "paragraph",
              "children": [
                {
                  "type": "text",
                  "value": "I’m a programatically generated figure from AST. See other figures..."
                }
              ]
            }
          ]
        }
     ]
  }
}, raw=True)
```
