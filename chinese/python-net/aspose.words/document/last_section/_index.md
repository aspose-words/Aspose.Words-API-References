---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /zh/python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# 空白文档默认包含一个节，
# 该节包含我们可以编辑的子节点。
self.assertEqual(1, doc.sections.count)
# 使用文档生成器向第一个节添加文本。
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# 通过插入节分隔符创建第二个节。
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# 每个节都有自己的页面设置。
# 我们可以将第二个节中的文本分成两列。
# 这不会影响第一个节中的文本。
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

