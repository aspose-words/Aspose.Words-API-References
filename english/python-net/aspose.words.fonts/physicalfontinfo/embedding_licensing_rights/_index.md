---
title: PhysicalFontInfo.embedding_licensing_rights property
linktitle: embedding_licensing_rights property
articleTitle: embedding_licensing_rights property
second_title: Aspose.Words for Python
description: "PhysicalFontInfo.embedding_licensing_rights property. Embedding licensing rights for the font."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/physicalfontinfo/embedding_licensing_rights/
---

## PhysicalFontInfo.embedding_licensing_rights property

Embedding licensing rights for the font.


```python
@property
def embedding_licensing_rights(self) -> aspose.words.fonts.FontEmbeddingLicensingRights:
    ...

```

### Examples

Shows how to get license rights information for embedded fonts (PhysicalFontInfo).

```python
settings = aw.fonts.FontSettings.default_instance
source = settings.get_fonts_sources()[0]
# Get the list of available fonts.
font_infos = source.get_available_fonts()
for font_info in font_infos:
    if font_info.embedding_licensing_rights != None:
        print(font_info.embedding_licensing_rights.embedding_usage_permissions)
        print(font_info.embedding_licensing_rights.bitmap_embedding_only)
        print(font_info.embedding_licensing_rights.no_subsetting)
```

### See Also

* module [aspose.words.fonts](../../)
* class [PhysicalFontInfo](../)

