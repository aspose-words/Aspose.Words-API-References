---
title: FontInfoCollection.embed_true_type_fonts property
linktitle: embed_true_type_fonts property
articleTitle: embed_true_type_fonts property
second_title: Aspose.Words for Python
description: "FontInfoCollection.embed_true_type_fonts property. Specifies whether or not to embed TrueType fonts in a document when it is saved"
type: docs
weight: 40
url: /python-net/aspose.words.fonts/fontinfocollection/embed_true_type_fonts/
---

## FontInfoCollection.embed_true_type_fonts property

Specifies whether or not to embed TrueType fonts in a document when it is saved.
Default value for this property is ``False``.


Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it,
but may substantially increase the document size.

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

