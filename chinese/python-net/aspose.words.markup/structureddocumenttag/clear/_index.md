---
title: StructuredDocumentTag.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.clear method. Clears contents of this structured document tag and displays a placeholder if it is defined."
type: docs
weight: 360
url: /zh/python-net/aspose.words.markup/structureddocumenttag/clear/
---

## clear() {#default}

Clears contents of this structured document tag and displays a placeholder if it is defined.


```python
def clear(self):
    ...
```

### Remarks

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [StructuredDocumentTag.xml_mapping](../xml_mapping/)
property), the referenced XML node is cleared.




### Examples

Shows how to delete contents of structured document tag elements.

```python
doc = aw.Document()
# 创建一个纯文本结构化文档标签，然后将其附加到文档中。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)
# 此结构化文档标签以文本框形式呈现，已显示占位符文本。
self.assertEqual('Click here to enter text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# 创建一个包含文本内容的构件块。
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'My placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.ensure_minimum()
substitute_block.first_section.body.first_paragraph.append_child(aw.Run(doc=glossary_doc, text='Custom placeholder text.'))
glossary_doc.append_child(substitute_block)
# 将结构化文档标签的 "PlaceholderName" 属性设置为我们的构件块名称，以获取
# 结构化文档标签显示构件块的内容，以替代原始默认文本。
tag.placeholder_name = 'My placeholder'
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# 编辑结构化文档标签的文本并隐藏占位符文本。
run = tag.get_child(aw.NodeType.RUN, 0, True).as_run()
run.text = 'New text.'
tag.is_showing_placeholder_text = False
self.assertEqual('New text.', tag.get_text().strip())
# 使用 "Clear" 方法清除此结构化文档标签的内容，并再次显示占位符。
tag.clear()
self.assertTrue(tag.is_showing_placeholder_text)
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

