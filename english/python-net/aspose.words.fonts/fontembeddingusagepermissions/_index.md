---
title: FontEmbeddingUsagePermissions enumeration
linktitle: FontEmbeddingUsagePermissions enumeration
articleTitle: FontEmbeddingUsagePermissions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontEmbeddingUsagePermissions enumeration. Represents the font embedding usage permissions."
type: docs
weight: 80
url: /python-net/aspose.words.fonts/fontembeddingusagepermissions/
---

## FontEmbeddingUsagePermissions enumeration

Represents the font embedding usage permissions.


### Members

| Name | Description |
| --- | --- |
| INSTALLABLE | The font may be embedded, and may be permanently installed for use on a remote systems, or for use by other users. |
| RESTRICTED_LICENSE | The font must not be modified, embedded or exchanged in any manner without first obtaining explicit permission of the legal owner. |
| PRINT_AND_PREVIEW | The font may be embedded, and may be temporarily loaded on other systems for purposes of viewing or printing the document. |
| EDITABLE | The font may be embedded, and may be temporarily loaded on other systems. |

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

* module [aspose.words.fonts](../)

