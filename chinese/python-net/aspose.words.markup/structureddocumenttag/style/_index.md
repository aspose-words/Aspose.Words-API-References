---
title: StructuredDocumentTag.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.style property. Gets or sets the Style of the structured document tag."
type: docs
weight: 260
url: /zh/python-net/aspose.words.markup/structureddocumenttag/style/
---

## StructuredDocumentTag.style property

Gets or sets the Style of the structured document tag.


```python
@property
def style(self) -> aspose.words.Style:
    ...

@style.setter
def style(self, value: aspose.words.Style):
    ...

```

### Remarks

Only [StyleType.CHARACTER](../../../aspose.words/styletype/#CHARACTER) style or [StyleType.PARAGRAPH](../../../aspose.words/styletype/#PARAGRAPH) style with linked character style can be set.



### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 下面介绍两种将文档中的样式应用到结构化文档标签的方法。
# 1 -  从文档的样式集合中应用样式对象：
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style
# 2 -  按名称引用文档中的样式：
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

