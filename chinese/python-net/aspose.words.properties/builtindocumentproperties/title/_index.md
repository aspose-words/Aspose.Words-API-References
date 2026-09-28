---
title: BuiltInDocumentProperties.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.title property. Gets or sets the title of the document."
type: docs
weight: 320
url: /zh/python-net/aspose.words.properties/builtindocumentproperties/title/
---

## BuiltInDocumentProperties.title property

Gets or sets the title of the document.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# 以下是四个内置文档属性，它们拥有可以在文档正文中显示其值的字段。
# 1 -  "Author" 属性，可使用 AUTHOR 字段显示：
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  "Title" 属性，可使用 TITLE 字段显示：
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  "Subject" 属性，可使用 SUBJECT 字段显示：
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  "Comments" 属性，可使用 COMMENTS 字段显示：
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# "Category" 内置属性没有可显示其值的字段。
properties.category = 'My category'
# 我们可以通过使用分号分隔 "Keywords" 属性的字符串值，为文档设置多个关键字。
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# 我们可以在 Windows 资源管理器中右键单击此文档，并在 "Properties" -> "Details" 中找到这些属性。
# "Author" 内置属性位于 "Origin" 组，其他属性位于 "Description" 组。
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

