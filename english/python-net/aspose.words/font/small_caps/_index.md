---
title: Font.small_caps property
linktitle: small_caps property
articleTitle: small_caps property
second_title: Aspose.Words for Python
description: "Font.small_caps property. True if the font is formatted as small capital letters."
type: docs
weight: 360
url: /python-net/aspose.words/font/small_caps/
---

## Font.small_caps property

True if the font is formatted as small capital letters.


```python
@property
def small_caps(self) -> bool:
    ...

@small_caps.setter
def small_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
# 1 -  Set the AllCaps flag to display all characters in regular capitals:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Set the SmallCaps flag to display all characters in small capitals:
# If a character is lower case, it will appear in its upper case form
# but will have the same height as the lower case (the font's x-height).
# Characters that were in upper case originally will look the same.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

