---
title: PageSetup.text_orientation property
linktitle: text_orientation property
articleTitle: text_orientation property
second_title: Aspose.Words for Python
description: "PageSetup.text_orientation property. Allows to specify [PageSetup.text_orientation](./) for the whole page"
type: docs
weight: 430
url: /python-net/aspose.words/pagesetup/text_orientation/
---

## PageSetup.text_orientation property

Allows to specify [PageSetup.text_orientation](./) for the whole page.
Default value is [TextOrientation.HORIZONTAL](../../textorientation/#HORIZONTAL)



```python
@property
def text_orientation(self) -> aspose.words.TextOrientation:
    ...

@text_orientation.setter
def text_orientation(self, value: aspose.words.TextOrientation):
    ...

```

### Remarks

This property is only supported for MS Word native formats DOCX, WML, RTF and DOC.


### Examples

Shows how to set text orientation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Set the "TextOrientation" property to "TextOrientation.Upward" to rotate all the text 90 degrees
# to the right so that all left-to-right text now goes top-to-bottom.
page_setup = doc.sections[0].page_setup
page_setup.text_orientation = aw.TextOrientation.UPWARD
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetTextOrientation.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

