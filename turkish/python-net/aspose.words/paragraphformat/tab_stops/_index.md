---
title: ParagraphFormat.tab_stops property
linktitle: tab_stops property
articleTitle: tab_stops property
second_title: Aspose.Words for Python
description: "ParagraphFormat.tab_stops property. Gets the collection of custom tab stops defined for this object."
type: docs
weight: 400
url: /tr/python-net/aspose.words/paragraphformat/tab_stops/
---

## ParagraphFormat.tab_stops property

Gets the collection of custom tab stops defined for this object.


```python
@property
def tab_stops(self) -> aspose.words.TabStopCollection:
    ...

```

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# TOC sonuç tabanlı stillere sahip tüm paragraflar arasında yineleme yapın; bu, TOC ile TOC9 arasındaki herhangi bir stildir.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # Bu paragrafta kullanılan ilk sekmeyi alın, bu sekme sayfa numaralarını hizalamak için kullanılmalıdır.
        tab = para.paragraph_format.tab_stops[0]
        # İlk varsayılan sekmeyi değiştirin, özel bir sekme durağıyla durdurun.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

