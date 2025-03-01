﻿---
title: FontInfoCollection.embed_system_fonts property
linktitle: embed_system_fonts property
articleTitle: embed_system_fonts property
second_title: Aspose.Words for Python
description: "FontInfoCollection.embed_system_fonts property. Specifies whether or not to embed System fonts into the document"
type: docs
weight: 30
url: /python-net/aspose.words.fonts/fontinfocollection/embed_system_fonts/
---

## FontInfoCollection.embed_system_fonts property

Specifies whether or not to embed System fonts into the document.
Default value for this property is ``False``.

This option works only when [FontInfoCollection.embed_true_type_fonts](../embed_true_type_fonts/) option is set to ``True``.




```python
@property
def embed_system_fonts(self) -> bool:
    ...

@embed_system_fonts.setter
def embed_system_fonts(self, value: bool):
    ...

```

### Remarks

Setting this property to ``True`` is useful if the user is on an East Asian system
and wants to create a document that is readable by others who do not have fonts for that
language on their system. For example, a user on a Japanese system could choose to embed the
fonts in a document so that the Japanese document would be readable on all systems.


This option works for DOC, DOCX and RTF formats only.




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

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfoCollection](../)

