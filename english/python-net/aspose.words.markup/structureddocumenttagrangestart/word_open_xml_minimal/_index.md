---
title: StructuredDocumentTagRangeStart.word_open_xml_minimal property
linktitle: word_open_xml_minimal property
articleTitle: word_open_xml_minimal property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.word_open_xml_minimal property. Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format."
type: docs
weight: 170
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/word_open_xml_minimal/
---

## StructuredDocumentTagRangeStart.word_open_xml_minimal property

Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.

Unlike the [StructuredDocumentTagRangeStart.word_open_xml](../word_open_xml/) property, this method generates a stripped-down document that excludes any non-content-related parts.



```python
@property
def word_open_xml_minimal(self) -> str:
    ...

```

### Examples

Shows how to get minimal XML contained within the node in the FlatOpc format.

```python
doc = aw.Document(MY_DIR + "Multi-section structured document tags.docx")


tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, True).as_structured_document_tag_range_start()
self.assertTrue(tag.word_open_xml_minimal.find( "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">") > 0)
self.assertTrue(tag.word_open_xml_minimal.find(
    "xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\"") < 0)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

