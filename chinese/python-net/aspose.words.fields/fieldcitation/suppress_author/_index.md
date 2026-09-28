---
title: FieldCitation.suppress_author property
linktitle: suppress_author property
articleTitle: suppress_author property
second_title: Aspose.Words for Python
description: "FieldCitation.suppress_author property. Gets or sets whether the author information is suppressed from the citation."
type: docs
weight: 80
url: /zh/python-net/aspose.words.fields/fieldcitation/suppress_author/
---

## FieldCitation.suppress_author property

Gets or sets whether the author information is suppressed from the citation.


```python
@property
def suppress_author(self) -> bool:
    ...

@suppress_author.setter
def suppress_author(self, value: bool):
    ...

```

### Examples

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```python
# 打开一个包含参考文献来源的文档，我们可以在其中找到
# Microsoft Word 的“引用”→“文献目录与参考文献”→“管理来源”。
doc = aw.Document(MY_DIR + 'Bibliography.docx')
builder = aw.DocumentBuilder(doc)
builder.write('Text to be cited with one source.')
# 创建仅包含页码和被引用书籍作者的引文。
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
# 我们使用它们的标签名称来引用来源。
field_citation.source_tag = 'Book1'
field_citation.page_number = '85'
field_citation.suppress_author = False
field_citation.suppress_title = True
field_citation.suppress_year = True
self.assertEqual(' CITATION  Book1 \\p 85 \\t \\y', field_citation.get_field_code())
# 创建一个更详细的引用，其中引用了两个来源。
builder.insert_paragraph()
builder.write('Text to be cited with two sources.')
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
field_citation.source_tag = 'Book1'
field_citation.another_source_tag = 'Book2'
field_citation.format_language_id = 'en-US'
field_citation.page_number = '19'
field_citation.prefix = 'Prefix '
field_citation.suffix = ' Suffix'
field_citation.suppress_author = False
field_citation.suppress_title = False
field_citation.suppress_year = False
field_citation.volume_number = 'VII'
self.assertEqual(' CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f "Prefix " \\s " Suffix" \\v VII', field_citation.get_field_code())
# 我们可以使用 BIBLIOGRAPHY 字段来显示文档中的所有来源。
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_bibliography = builder.insert_field(aw.fields.FieldType.FIELD_BIBLIOGRAPHY, True).as_field_bibliography()
field_bibliography.format_language_id = '5129'
self.assertEqual(' BIBLIOGRAPHY  \\l 5129', field_bibliography.get_field_code())
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_citation.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCitation](../)

