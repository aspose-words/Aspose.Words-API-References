---
title: FontEmbeddingLicensingRights.bitmap_embedding_only property
linktitle: bitmap_embedding_only property
articleTitle: bitmap_embedding_only property
second_title: Aspose.Words for Python
description: "FontEmbeddingLicensingRights.bitmap_embedding_only property. Indicates the Bitmap embedding only restriction."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/fontembeddinglicensingrights/bitmap_embedding_only/
---

## FontEmbeddingLicensingRights.bitmap_embedding_only property

Indicates the "Bitmap embedding only" restriction.


```python
@property
def bitmap_embedding_only(self) -> bool:
    ...

```

### Remarks

When this bit is set, only bitmaps contained in the font may be embedded. No outline data may be embedded.
If there are no bitmaps available in the font, then the font is considered unembeddable and the embedding
services will fail. Other embedding restrictions also apply.


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
* class [FontEmbeddingLicensingRights](../)

