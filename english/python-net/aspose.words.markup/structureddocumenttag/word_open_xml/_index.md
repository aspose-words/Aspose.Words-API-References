---
title: StructuredDocumentTag.word_open_xml property
linktitle: word_open_xml property
articleTitle: word_open_xml property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.word_open_xml property. Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format."
type: docs
weight: 300
url: /python-net/aspose.words.markup/structureddocumenttag/word_open_xml/
---

## StructuredDocumentTag.word_open_xml property

Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.



### Examples

Shows how to get XML contained within the node in the FlatOpc format.

```python
doc = aw.Document(MY_DIR + "Structured document tags.docx")

tags = [node.as_structured_document_tag()
        for node in doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)]

self.assertIn(
    "<pkg:part pkg:name=\"/docProps/app.xml\" pkg:contentType=\"application/vnd.openxmlformats-officedocument.extended-properties+xml\">",
    tags[0].word_open_xml)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

