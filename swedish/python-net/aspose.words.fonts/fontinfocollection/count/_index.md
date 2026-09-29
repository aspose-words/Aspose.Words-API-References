---
title: FontInfoCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "FontInfoCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fonts/fontinfocollection/count/
---

## FontInfoCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows info about the fonts that are present in the blank document.

```python
doc = aw.Document()
# Ett tomt dokument innehåller 3 standardteckensnitt. Varje teckensnitt i dokumentet
# kommer att ha ett motsvarande FontInfo‑objekt som innehåller detaljer om det teckensnittet.
self.assertEqual(3, doc.font_infos.count)
self.assertTrue(doc.font_infos.contains('Times New Roman'))
self.assertEqual(204, doc.font_infos.get_by_name('Times New Roman').charset)
self.assertTrue(doc.font_infos.contains('Symbol'))
self.assertTrue(doc.font_infos.contains('Arial'))
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

