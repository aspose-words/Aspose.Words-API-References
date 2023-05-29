---
title: FontInfoCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "FontInfoCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/fontinfocollection/count/
---

## FontInfoCollection.count property

Gets the number of elements contained in the collection.


### Examples

Shows info about the fonts that are present in the blank document.

```python
doc = aw.Document()

# A blank document contains 3 default fonts. Each font in the document
# will have a corresponding FontInfo object which contains details about that font.
self.assertEqual(3, doc.font_infos.count)

font_names = [font.name for font in doc.font_infos]
self.assertIn("Times New Roman", font_names)
self.assertEqual(204, doc.font_infos.get_by_name("Times New Roman").charset)

self.assertIn("Symbol", font_names)
self.assertIn("Arial", font_names)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

