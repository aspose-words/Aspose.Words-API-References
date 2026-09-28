---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /zh/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# 插入一个纯文本结构化文档标签，
# 它将充当用户可以输入文本的纯文本表单。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# 将 "IsTemporary" 属性设置为 "true" 以使结构化文档标签消失并
# 在用户在 Microsoft Word 中编辑一次后，将其内容合并到文档中。
# 将 "IsTemporary" 属性设置为 "false" 以允许用户编辑内容
# 结构化文档标签的内容任意次数。
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# 插入另一个以复选框形式的结构化文档标签，并将其默认状态设置为 "checked"。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# 将 "IsTemporary" 属性设置为 "true" 使复选框变成符号
# 一旦用户在 Microsoft Word 中点击它。
# 将 "IsTemporary" 属性设置为 "false" 以允许用户任意次数点击复选框。
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

