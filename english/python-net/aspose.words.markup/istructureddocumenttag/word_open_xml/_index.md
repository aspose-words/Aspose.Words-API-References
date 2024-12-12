---
title: IStructuredDocumentTag.word_open_xml property
linktitle: word_open_xml property
articleTitle: word_open_xml property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.word_open_xml property. Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format."
type: docs
weight: 150
url: /python-net/aspose.words.markup/istructureddocumenttag/word_open_xml/
---

## IStructuredDocumentTag.word_open_xml property

Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.



```python
@property
def word_open_xml(self) -> str:
    ...

```

### Examples

Shows how to get XML contained within the node in the FlatOpc format.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
tags = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_structured_document_tag(), b), list(doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)))))
self.assertTrue('<pkg:part pkg:name="/docProps/app.xml" pkg:contentType="application/vnd.openxmlformats-officedocument.extended-properties+xml">' in tags[0].word_open_xml)
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

