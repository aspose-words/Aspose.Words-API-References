---
title: FontInfoCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "FontInfoCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fonts/fontinfocollection/count/
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
# Boş bir belge 3 varsayılan yazı tipi içerir. Belgedeki her yazı tipi
# o yazı tipi hakkında ayrıntılar içeren ilgili bir FontInfo nesnesine sahip olacaktır.
self.assertEqual(3, doc.font_infos.count)
self.assertTrue(doc.font_infos.contains('Times New Roman'))
self.assertEqual(204, doc.font_infos.get_by_name('Times New Roman').charset)
self.assertTrue(doc.font_infos.contains('Symbol'))
self.assertTrue(doc.font_infos.contains('Arial'))
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

