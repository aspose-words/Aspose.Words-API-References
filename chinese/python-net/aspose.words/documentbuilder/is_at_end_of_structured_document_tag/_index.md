---
title: DocumentBuilder.is_at_end_of_structured_document_tag property
linktitle: is_at_end_of_structured_document_tag property
articleTitle: is_at_end_of_structured_document_tag property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_structured_document_tag property. Returns true if the cursor is at the end of a structured document tag."
type: docs
weight: 120
url: /zh/python-net/aspose.words/documentbuilder/is_at_end_of_structured_document_tag/
---

## DocumentBuilder.is_at_end_of_structured_document_tag property

Returns **true** if the cursor is at the end of a structured document tag.



```python
@property
def is_at_end_of_structured_document_tag(self) -> bool:
    ...

```

### Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
builder = aw.DocumentBuilder(doc=doc)
# 有几种方法可以移动光标：
# 1 - 通过索引移动到结构化文档标签的第一个字符。
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=1)
# 2 - 通过对象移动到结构化文档标签的第一个字符。
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(structured_document_tag=tag, character_index=1)
builder.write(' New text.')
self.assertEqual('R New text.ichText', tag.get_text().strip())
# 3 - 移动到第二个结构化文档标签的末尾。
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=-1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)
# 获取当前选中的结构化文档标签。
builder.current_structured_document_tag.color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Document.MoveToStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

