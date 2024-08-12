---
title: FontEmbeddingLicensingRights.no_subsetting property
linktitle: no_subsetting property
articleTitle: no_subsetting property
second_title: Aspose.Words for Python
description: "FontEmbeddingLicensingRights.no_subsetting property. Indicates the No subsetting restriction."
type: docs
weight: 30
url: /python-net/aspose.words.fonts/fontembeddinglicensingrights/no_subsetting/
---

## FontEmbeddingLicensingRights.no_subsetting property

Indicates the "No subsetting" restriction.


```python
@property
def no_subsetting(self) -> bool:
    ...

```

### Remarks

When this flag is set, the font must not be subsetted prior to embedding. Other embedding restrictions
also apply.


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

