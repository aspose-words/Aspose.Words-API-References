---
title: StructuredDocumentTag.word_open_xml_minimal property
linktitle: word_open_xml_minimal property
articleTitle: word_open_xml_minimal property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.word_open_xml_minimal property. Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format."
type: docs
weight: 310
url: /python-net/aspose.words.markup/structureddocumenttag/word_open_xml_minimal/
---

## StructuredDocumentTag.word_open_xml_minimal property

Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.

Unlike the [StructuredDocumentTag.word_open_xml](../word_open_xml/) property, this method generates a stripped-down document that excludes any non-content-related parts.



### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two ways to apply a style from the document to a structured document tag.
# 1 -  Apply a style object from the document's style collection:
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style

# 2 -  Reference a style in the document by name:
sdt_rich_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.RICH_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_rich_text.style_name = "Quote"

builder.insert_node(sdt_plain_text)
builder.insert_node(sdt_rich_text)

self.assertEqual(aw.NodeType.STRUCTURED_DOCUMENT_TAG, sdt_plain_text.node_type)

tags = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)

for node in tags:
    sdt = node.as_structured_document_tag()
    print(sdt.word_open_xml_minimal)
    self.assertEqual(aw.StyleIdentifier.QUOTE, sdt.style.style_identifier)
    self.assertEqual("Quote", sdt.style_name)
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

