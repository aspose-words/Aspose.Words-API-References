---
title: FontEmbeddingLicensingRights.embedding_usage_permissions property
linktitle: embedding_usage_permissions property
articleTitle: embedding_usage_permissions property
second_title: Aspose.Words for Python
description: "FontEmbeddingLicensingRights.embedding_usage_permissions property. Usage permissions."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/fontembeddinglicensingrights/embedding_usage_permissions/
---

## FontEmbeddingLicensingRights.embedding_usage_permissions property

Usage permissions.


```python
@property
def embedding_usage_permissions(self) -> aspose.words.fonts.FontEmbeddingUsagePermissions:
    ...

```

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

