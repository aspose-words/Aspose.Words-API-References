---
title: PageSetup.text_orientation property
linktitle: text_orientation property
articleTitle: text_orientation property
second_title: Aspose.Words for Python
description: "PageSetup.text_orientation property. Allows to specify [PageSetup.text_orientation](./) for the whole page"
type: docs
weight: 430
url: /zh/python-net/aspose.words/pagesetup/text_orientation/
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
# 将 \"TextOrientation\" 属性设置为 \"TextOrientation.Upward\"，以将所有文本旋转 90 度
# 向右，使所有从左到右的文本现在从上到下排列。
page_setup = doc.sections[0].page_setup
page_setup.text_orientation = aw.TextOrientation.UPWARD
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetTextOrientation.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

