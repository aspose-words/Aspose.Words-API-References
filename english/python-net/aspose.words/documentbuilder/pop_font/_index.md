---
title: pop_font method
second_title: Aspose.Words for Python via .NET API Reference
description: "Retrieves character formatting previously saved on the stack."
type: docs
weight: 590
url: /python-net/aspose.words/documentbuilder/pop_font/
---

## pop_font() {#default}

Retrieves character formatting previously saved on the stack.


```python
def pop_font(self):
    ...
```

### Examples

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set up font formatting, then write the text that goes before the hyperlink.
builder.font.name = "Arial"
builder.font.size = 24
builder.write("To visit Google, hold Ctrl and click ")

# Preserve our current formatting configuration on the stack.
builder.push_font()

# Alter the builder's current formatting by applying a new style.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink("here", "http://www.google.com", False)

self.assertEqual(drawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)

# Restore the font formatting that we saved earlier and remove the element from the stack.
builder.pop_font()

self.assertEqual(drawing.Color.empty().to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.NONE, builder.font.underline)

builder.write(". We hope you enjoyed the example.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.push_pop_font.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)
* property [DocumentBuilder.font](../font/)
* method [DocumentBuilder.push_font()](../push_font/#default)

