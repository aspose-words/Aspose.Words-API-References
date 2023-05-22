﻿---
title: FontInfoCollection class
linktitle: FontInfoCollection class
articleTitle: FontInfoCollection class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontInfoCollection class. Represents a collection of fonts used in a document"
type: docs
weight: 100
url: /python-net/aspose.words.fonts/fontinfocollection/
---

## FontInfoCollection class

Represents a collection of fonts used in a document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




Items are [FontInfo](../fontinfo/) objects.

You do not create instances of this class directly. 
Use the [DocumentBase.font_infos](../../aspose.words/documentbase/font_infos/) property to access the collection of fonts 
defined in the document.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a font at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [embed_system_fonts](./embed_system_fonts/) | Specifies whether or not to embed System fonts into the document. Default value for this property is ``False``. |
| [embed_true_type_fonts](./embed_true_type_fonts/) | Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is ``False``. |
| [save_subset_fonts](./save_subset_fonts/) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is ``False``. |

### Methods

| Name | Description |
| --- | --- |
|[ contains(name)](./contains/#str) | Determines whether the collection contains a font with the given name. |
|[ get_by_name(name)](./get_by_name/#str) | Gets a font with the specified name. |

### Examples

Shows how to print the details of what fonts are present in a document.

```python
doc = aw.Document(MY_DIR + "Embedded font.docx")

all_fonts = doc.font_infos

# Print all the used and unused fonts in the document.
for i in range(all_fonts.count):
    print(f"Font index #{i}")
    print(f"\tName: {all_fonts[i].name}")
    print(f'\tIs {"" if all_fonts[i].is_true_type else "not "}a TrueType font')
```

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

* module [aspose.words.fonts](../)
* class [FontInfo](../fontinfo/)
* property [DocumentBase.font_infos](../../aspose.words/documentbase/font_infos/)

