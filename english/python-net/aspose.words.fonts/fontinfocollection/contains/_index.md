---
title: FontInfoCollection.contains method
linktitle: contains method
articleTitle: contains method
second_title: Aspose.Words for Python
description: "FontInfoCollection.contains method. Determines whether the collection contains a font with the given name."
type: docs
weight: 60
url: /python-net/aspose.words.fonts/fontinfocollection/contains/
---

## contains(name) {#str}

Determines whether the collection contains a font with the given name.


```python
def contains(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | Case-insensitive name of the font to locate. |

### Returns

``True`` if the item is found in the collection; otherwise, ``False``.


### Examples

Shows info about the fonts that are present in the blank document.

```python
doc = aw.Document()
# A blank document contains 3 default fonts. Each font in the document
# will have a corresponding FontInfo object which contains details about that font.
self.assertEqual(3, doc.font_infos.count)
self.assertTrue(doc.font_infos.contains('Times New Roman'))
self.assertEqual(204, doc.font_infos.get_by_name('Times New Roman').charset)
self.assertTrue(doc.font_infos.contains('Symbol'))
self.assertTrue(doc.font_infos.contains('Arial'))
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

