---
title: text_orientation property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify [PageSetup.text_orientation](./) for the whole page"
type: docs
weight: 420
url: /python-net/aspose.words/pagesetup/text_orientation/
---

## PageSetup.text_orientation property

Allows to specify [PageSetup.text_orientation](./) for the whole page.
Default value is [TextOrientation.HORIZONTAL](../../textorientation/#HORIZONTAL)

This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.


### Examples

Shows how to set text orientation.

```python
doc = aw.Document()

builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Set the "text_orientation" property to "TextOrientation.UPWARD" to rotate all the text 90 degrees
# to the right so that all left-to-right text now goes top-to-bottom.
page_setup = doc.sections[0].page_setup
page_setup.text_orientation = aw.TextOrientation.UPWARD

doc.save(ARTIFACTS_DIR + "PageSetup.set_text_orientation.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

