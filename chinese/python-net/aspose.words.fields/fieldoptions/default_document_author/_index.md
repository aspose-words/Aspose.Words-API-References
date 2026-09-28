---
title: FieldOptions.default_document_author property
linktitle: default_document_author property
articleTitle: default_document_author property
second_title: Aspose.Words for Python
description: "FieldOptions.default_document_author property. Gets or sets default document author's name"
type: docs
weight: 70
url: /zh/python-net/aspose.words.fields/fieldoptions/default_document_author/
---

## FieldOptions.default_document_author property

Gets or sets default document author's name. If author's name is already specified in built-in document properties,
this option is not considered.


```python
@property
def default_document_author(self) -> str:
    ...

@default_document_author.setter
def default_document_author(self, value: str):
    ...

```

### Examples

Shows how to use an AUTHOR field to display a document creator's name.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# AUTHOR 字段从名为 "Author" 的内置文档属性获取结果。
# 如果我们在 Microsoft Word 中创建并保存文档，
# 该属性中将会是我们的用户名。
# 然而，如果我们使用 Aspose.Words 以编程方式创建文档，
# 默认情况下，"Author" 属性将是空字符串。
self.assertEqual('', doc.built_in_document_properties.author)
# 设置 AUTHOR 字段使用的备用作者名称
# 如果 "Author" 属性包含空字符串。
doc.field_options.default_document_author = 'Joe Bloggs'
builder.write('This document was created by ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('Joe Bloggs', field.result)
# 更新包含值的 AUTHOR 字段
# 将把该值应用到 "Author" 内置属性。
self.assertEqual('Joe Bloggs', doc.built_in_document_properties.author)
# 更改此属性后，再更新 AUTHOR 字段将把该值应用到字段。
doc.built_in_document_properties.author = 'John Doe'
field.update()
self.assertEqual(' AUTHOR ', field.get_field_code())
self.assertEqual('John Doe', field.result)
# 如果我们在更改其 "Name" 属性后更新 AUTHOR 字段，
# 则字段将显示新名称并将新名称应用到内置属性。
field.author_name = 'Jane Doe'
field.update()
self.assertEqual(' AUTHOR  "Jane Doe"', field.get_field_code())
self.assertEqual('Jane Doe', field.result)
# AUTHOR 字段不会影响 DefaultDocumentAuthor 属性。
self.assertEqual('Jane Doe', doc.built_in_document_properties.author)
self.assertEqual('Joe Bloggs', doc.field_options.default_document_author)
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTHOR.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

