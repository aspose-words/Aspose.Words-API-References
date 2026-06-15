---
title: CustomXmlPart.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "CustomXmlPart.id property. Gets or sets the string that identifies this custom XML part within an OOXML document."
type: docs
weight: 40
url: /python-net/aspose.words.markup/customxmlpart/id/
---

## CustomXmlPart.id property

Gets or sets the string that identifies this custom XML part within an OOXML document.


```python
@property
def id(self) -> str:
    ...

@id.setter
def id(self, value: str):
    ...

```

### Remarks

ISO/IEC 29500 specifies that this value is a GUID, but old versions of Microsoft Word allowed any
string here. Aspose.Words does the same for ECMA-376 format. But note, that Microsoft Word Online fails 
to open a document created with a non-GUID value. So, a GUID is preferred value for this property.

A valid value must be an identifier that is unique among all custom XML data parts in this document.

The default value is an empty string. The value cannot be ``None``.




### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPart](../)

