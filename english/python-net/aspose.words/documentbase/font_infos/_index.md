---
title: DocumentBase.font_infos property
linktitle: font_infos property
articleTitle: font_infos property
second_title: Aspose.Words for Python
description: "DocumentBase.font_infos property. Provides access to properties of fonts used in this document."
type: docs
weight: 30
url: /python-net/aspose.words/documentbase/font_infos/
---

## DocumentBase.font_infos property

Provides access to properties of fonts used in this document.


```python
@property
def font_infos(self) -> aspose.words.fonts.FontInfoCollection:
    ...

```

### Remarks

This collection of font definitions is loaded as is from the document.
Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document.
You should only use this collection to get information about fonts that might be used in the document.




### Examples

Shows how to save a document with embedded TrueType fonts.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
font_infos = doc.font_infos
font_infos.embed_true_type_fonts = embed_all_fonts
font_infos.embed_system_fonts = embed_all_fonts
font_infos.save_subset_fonts = embed_all_fonts
doc.save(file_name=ARTIFACTS_DIR + 'Font.FontInfoCollection.docx')
```

Shows how to print the details of what fonts are present in a document.

```python
doc = aw.Document(MY_DIR + 'Embedded font.docx')
all_fonts = doc.font_infos
# Print all the used and unused fonts in the document.
for i in range(all_fonts.count):
    print(f'Font index #{i}')
    print(f'\tName: {all_fonts[i].name}')
    print(f"\tIs {('' if all_fonts[i].is_true_type else 'not ')}a TrueType font")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [FontInfo](../../../aspose.words.fonts/fontinfo/)

