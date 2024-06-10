---
title: LayoutOptions.show_hidden_text property
linktitle: show_hidden_text property
articleTitle: show_hidden_text property
second_title: Aspose.Words for Python
description: "LayoutOptions.show_hidden_text property. Gets or sets indication of whether hidden text in the document is rendered"
type: docs
weight: 80
url: /python-net/aspose.words.layout/layoutoptions/show_hidden_text/
---

## LayoutOptions.show_hidden_text property

Gets or sets indication of whether hidden text in the document is rendered.
Default is ``False``.



```python
@property
def show_hidden_text(self) -> bool:
    ...

@show_hidden_text.setter
def show_hidden_text(self, value: bool):
    ...

```

### Remarks

This property affects all hidden content, not just text.


### Examples

Shows how to hide text in a rendered output document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert hidden text, then specify whether we wish to omit it from a rendered document.
builder.writeln('This text is not hidden.')
builder.font.hidden = True
builder.writeln('This text is hidden.')
doc.layout_options.show_hidden_text = show_hidden_text
doc.save(ARTIFACTS_DIR + 'Document.layout_options_hidden_text.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

