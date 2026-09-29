---
title: Font.all_caps property
linktitle: all_caps property
articleTitle: all_caps property
second_title: Aspose.Words for Python
description: "Font.all_caps property. True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /sv/python-net/aspose.words/font/all_caps/
---

## Font.all_caps property

True if the font is formatted as all capital letters.


```python
@property
def all_caps(self) -> bool:
    ...

@all_caps.setter
def all_caps(self, value: bool):
    ...

```

### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()
# Det finns två sätt att få ett körsegment att visa sin gemena text i versaler utan att ändra innehållet.
# 1 -  Ställ in AllCaps-flaggan för att visa alla tecken i vanliga versaler:
run = aw.Run(doc=doc, text='all capitals')
run.font.all_caps = True
para.append_child(run)
para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()
# 2 -  Ställ in SmallCaps-flaggan för att visa alla tecken i små versaler:
# Om ett tecken är gemener kommer det att visas i sin versalform
# men kommer att ha samma höjd som gemener (teckensnittets x-höjd).
# Tecken som ursprungligen var versaler kommer att se likadana ut.
run = aw.Run(doc=doc, text='Small Capitals')
run.font.small_caps = True
para.append_child(run)
doc.save(file_name=ARTIFACTS_DIR + 'Font.Caps.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

