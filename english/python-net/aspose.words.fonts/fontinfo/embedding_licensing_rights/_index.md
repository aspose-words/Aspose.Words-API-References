---
title: FontInfo.embedding_licensing_rights property
linktitle: embedding_licensing_rights property
articleTitle: embedding_licensing_rights property
second_title: Aspose.Words for Python
description: "FontInfo.embedding_licensing_rights property. Gets the embedded font licensing rights."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/fontinfo/embedding_licensing_rights/
---

## FontInfo.embedding_licensing_rights property

Gets the embedded font licensing rights.


```python
@property
def embedding_licensing_rights(self) -> aspose.words.fonts.FontEmbeddingLicensingRights:
    ...

```

### Remarks

The value may be null if font is not embedded.




### Examples

Shows how to get license rights information for embedded fonts (FontInfo).

```python
doc = aw.Document(file_name=MY_DIR + 'Embedded font rights.docx')
# Get the list of document fonts.
font_infos = doc.font_infos
for font_info in font_infos:
    if font_info.embedding_licensing_rights != None:
        print(font_info.embedding_licensing_rights.embedding_usage_permissions)
        print(font_info.embedding_licensing_rights.bitmap_embedding_only)
        print(font_info.embedding_licensing_rights.no_subsetting)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontInfo](../)

