---
title: FontEmbeddingLicensingRights class
linktitle: FontEmbeddingLicensingRights class
articleTitle: FontEmbeddingLicensingRights class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontEmbeddingLicensingRights class. Represents embedding licensing rights for the font."
type: docs
weight: 70
url: /python-net/aspose.words.fonts/fontembeddinglicensingrights/
---

## FontEmbeddingLicensingRights class

Represents embedding licensing rights for the font.


### Remarks

To learn more, visit the
[OpenType specification section](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype)
on Microsoft Typography portal.



### Properties

| Name | Description |
| --- | --- |
| [bitmap_embedding_only](./bitmap_embedding_only/) | Indicates the "Bitmap embedding only" restriction. |
| [embedding_usage_permissions](./embedding_usage_permissions/) | Usage permissions. |
| [no_subsetting](./no_subsetting/) | Indicates the "No subsetting" restriction. |

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

