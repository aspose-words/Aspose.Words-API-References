---
title: Font.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Font.hidden property. True if the font is formatted as hidden text."
type: docs
weight: 140
url: /python-net/aspose.words/font/hidden/
---

## Font.hidden property

True if the font is formatted as hidden text.


### Examples

Shows how to create a run of hidden text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# With the "hidden" flag set to True, any text that we create using this Font object will be invisible in the document.
# We will not see or highlight hidden text unless we enable the "Hidden text" option
# found in Microsoft Word via "File" -> "Options" -> "Display". The text will still be there,
# and we will be able to access this text programmatically.
# It is not advised to use this method to hide sensitive information.
builder.font.hidden = True
builder.font.size = 36

builder.writeln("This text will not be visible in the document.")

doc.save(ARTIFACTS_DIR + "Font.hidden.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

