---
title: MarkupLevel enumeration
linktitle: MarkupLevel enumeration
articleTitle: MarkupLevel enumeration
second_title: Aspose.Words for Python
description: "aspose.words.markup.MarkupLevel enumeration. Specifies the level in the document tree where a particular [StructuredDocumentTag](../structureddocumenttag/) can occur."
type: docs
weight: 90
url: /it/python-net/aspose.words.markup/markuplevel/
---

## MarkupLevel enumeration

Specifies the level in the document tree where a particular [StructuredDocumentTag](../structureddocumenttag/) can occur.



### Members

| Name | Description |
| --- | --- |
| UNKNOWN | Specifies the unknown or invalid value. |
| INLINE | The element occurs at the inline level (e.g. among as runs of text). |
| BLOCK | The element occurs at the block level (e.g. among tables and paragraphs). |
| ROW | The element occurs among rows in a table. |
| CELL | The element occurs among cells in a row. |

### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Di seguito sono due modi per applicare uno stile dal documento a un tag di documento strutturato.
# 1 -  Applica un oggetto stile dalla raccolta di stili del documento:
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style
# 2 -  Riferisci uno stile nel documento per nome:
sdt_rich_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.RICH_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_rich_text.style_name = 'Quote'
builder.insert_node(sdt_plain_text)
builder.insert_node(sdt_rich_text)
self.assertEqual(aw.NodeType.STRUCTURED_DOCUMENT_TAG, sdt_plain_text.node_type)
tags = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)
for node in tags:
    sdt = node.as_structured_document_tag()
    print(sdt.word_open_xml_minimal)
    self.assertEqual(aw.StyleIdentifier.QUOTE, sdt.style.style_identifier)
    self.assertEqual('Quote', sdt.style_name)
```

### See Also

* module [aspose.words.markup](../)

