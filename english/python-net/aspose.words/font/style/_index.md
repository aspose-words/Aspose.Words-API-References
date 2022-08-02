---
title: style property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the character style applied to this formatting."
type: docs
weight: 400
url: /python-net/aspose.words/font/style/
---

## Font.style property

Gets or sets the character style applied to this formatting.


### Examples

Applies a double underline to all runs in a document that are formatted with custom character styles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a custom style and apply it to text created using a document builder.
style = doc.styles.add(aw.StyleType.CHARACTER, "MyStyle")
style.font.color = drawing.Color.red
style.font.name = "Courier New"

builder.font.style_name = "MyStyle"
builder.write("This text is in a custom style.")

# Iterate over every run and add a double underline to every custom style.
for run in doc.get_child_nodes(aw.NodeType.RUN, True):
    run = run.as_run()

    char_style = run.font.style

    if not char_style.built_in:
        run.font.underline = aw.Underline.DOUBLE

doc.save(ARTIFACTS_DIR + "Font.style.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

