---
title: StructuredDocumentTag.placeholder_name property
linktitle: placeholder_name property
articleTitle: placeholder_name property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.placeholder_name property. Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text."
type: docs
weight: 240
url: /zh/python-net/aspose.words.markup/structureddocumenttag/placeholder_name/
---

## StructuredDocumentTag.placeholder_name property

Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.




```python
@property
def placeholder_name(self) -> str:
    ...

@placeholder_name.setter
def placeholder_name(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [Document.glossary_document](../../../aspose.words/document/glossary_document/). |

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# 插入一种 "PlainText" 类型的纯文本结构化文档标签，它将作为文本框使用。
# 它默认显示的内容是一个 "Click here to enter text." 提示。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# 我们可以让标签显示构建块的内容，而不是默认文本。
# 首先，向词汇表文档添加一个包含内容的构建块。
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# 然后，使用结构化文档标签的 "PlaceholderName" 属性按名称引用该构建块。
tag.placeholder_name = 'Custom Placeholder'
# 如果 "PlaceholderName" 引用父文档词汇表文档中已有的块，
# 我们将能够通过 "Placeholder" 属性验证该构建块。
self.assertEqual(substitute_block, tag.placeholder)
# 将 "IsShowingPlaceholderText" 属性设置为 "true"，以将
# 结构化文档标签当前的内容视为占位符文本。
# 这意味着在 Microsoft Word 中单击文本框会立即突出显示标签的所有内容。
# 将 "IsShowingPlaceholderText" 属性设置为 "false"，以使
# 结构化文档标签将其内容视为用户已输入的文本。
# 在 Microsoft Word 中单击此文本会将闪烁的光标放置在点击位置。
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

