---
title: FontInfoCollection.save_subset_fonts property
linktitle: save_subset_fonts property
articleTitle: save_subset_fonts property
second_title: Aspose.Words for Python
description: "FontInfoCollection.save_subset_fonts property. Specifies whether or not to save a subset of the embedded TrueType fonts with the document"
type: docs
weight: 50
url: /python-net/aspose.words.fonts/fontinfocollection/save_subset_fonts/
---

## FontInfoCollection.save_subset_fonts property

Specifies whether or not to save a subset of the embedded TrueType fonts with the document.
Default value for this property is ``False``.

This option works only when [FontInfoCollection.embed_true_type_fonts](../embed_true_type_fonts/) property is set to ``True``.




```python
@property
def save_subset_fonts(self) -> bool:
    ...

@save_subset_fonts.setter
def save_subset_fonts(self, value: bool):
    ...

```

### Remarks

This option works for DOC, DOCX and RTF formats only.


### Examples

Shows how to save a document with embedded TrueType fonts.

```python
doc = aw.Document(MY_DIR + "Document.docx")

font_infos = doc.font_infos
font_infos.embed_true_type_fonts = embed_all_fonts
font_infos.embed_system_fonts = embed_all_fonts
font_infos.save_subset_fonts = embed_all_fonts

doc.save(ARTIFACTS_DIR + "Font.font_info_collection.docx")

if embed_all_fonts:
    self.assertLess(25000, os.path.getsize(ARTIFACTS_DIR + "Font.font_info_collection.docx"))
else:
    self.assertGreater(15000, os.path.getsize(ARTIFACTS_DIR + "Font.font_info_collection.docx"))
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

