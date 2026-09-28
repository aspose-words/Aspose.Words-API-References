---
title: StructuredDocumentTag.lock_content_control property
linktitle: lock_content_control property
articleTitle: lock_content_control property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.lock_content_control property. When set to ``True``, this property will prohibit a user from deleting this SDT."
type: docs
weight: 190
url: /zh/python-net/aspose.words.markup/structureddocumenttag/lock_content_control/
---

## StructuredDocumentTag.lock_content_control property

When set to ``True``, this property will prohibit a user from deleting this **SDT**.



```python
@property
def lock_content_control(self) -> bool:
    ...

@lock_content_control.setter
def lock_content_control(self, value: bool):
    ...

```

### Examples

Shows how to apply editing restrictions to structured document tags.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个纯文本结构化文档标签，它充当提示用户填写的文本框。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# 将 "LockContents" 属性设置为 "true"，以禁止用户编辑此文本框的内容。
tag.lock_contents = True
builder.write('The contents of this structured document tag cannot be edited: ')
builder.insert_node(tag)
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# 将 "LockContentControl" 属性设置为 "true"，以禁止用户
# 在 Microsoft Word 中手动删除此结构化文档标签。
tag.lock_content_control = True
builder.insert_paragraph()
builder.write('This structured document tag cannot be deleted but its contents can be edited: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.Lock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

