---
title: StructuredDocumentTag.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.node_type property. Returns [NodeType.STRUCTURED_DOCUMENT_TAG](../../../aspose.words/nodetype/#STRUCTURED_DOCUMENT_TAG)."
type: docs
weight: 220
url: /es/python-net/aspose.words.markup/structureddocumenttag/node_type/
---

## StructuredDocumentTag.node_type property

Returns [NodeType.STRUCTURED_DOCUMENT_TAG](../../../aspose.words/nodetype/#STRUCTURED_DOCUMENT_TAG).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# A continuación se presentan dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
# 1 -  Aplicar un objeto de estilo de la colección de estilos del documento:
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style
# 2 -  Referenciar un estilo en el documento por nombre:
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

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

