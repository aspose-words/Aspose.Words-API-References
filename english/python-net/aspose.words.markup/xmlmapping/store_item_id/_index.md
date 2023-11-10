---
title: XmlMapping.store_item_id property
linktitle: store_item_id property
articleTitle: store_item_id property
second_title: Aspose.Words for Python
description: "XmlMapping.store_item_id property. Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XmlMapping.xpath](../xpath/) expression."
type: docs
weight: 40
url: /python-net/aspose.words.markup/xmlmapping/store_item_id/
---

## XmlMapping.store_item_id property

Specifies the custom XML data identifier for the custom XML data part which
shall be used to evaluate the [XmlMapping.xpath](../xpath/) expression.



```python
@property
def store_item_id(self) -> str:
    ...

```

### Examples

Shows how to get the custom XML data identifier of an XML part.

```python
doc = aw.Document(MY_DIR + "Custom XML part in structured document tag.docx")

# Structured document tags have IDs in the form of GUIDs.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 0, True).as_structured_document_tag()

self.assertEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.xml_mapping.store_item_id)
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

