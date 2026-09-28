---
title: BuiltInDocumentProperties.category property
linktitle: category property
articleTitle: category property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.category property. Gets or sets the category of the document."
type: docs
weight: 40
url: /ar/python-net/aspose.words.properties/builtindocumentproperties/category/
---

## BuiltInDocumentProperties.category property

Gets or sets the category of the document.


```python
@property
def category(self) -> str:
    ...

@category.setter
def category(self, value: str):
    ...

```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
properties = doc.built_in_document_properties
# فيما يلي أربع خصائص مدمجة للمستند لديها حقول يمكنها عرض قيمها في جسم المستند.
# 1 -  الخاصية "Author"، التي يمكننا عرضها باستخدام حقل AUTHOR:
properties.author = 'John Doe'
builder.write('Author:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True)
# 2 -  الخاصية "Title"، التي يمكننا عرضها باستخدام حقل TITLE:
properties.title = "John's Document"
builder.write('\nDoc title:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=True)
# 3 -  الخاصية "Subject"، التي يمكننا عرضها باستخدام حقل SUBJECT:
properties.subject = 'My subject'
builder.write('\nSubject:\t')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_SUBJECT, update_field=True)
# 4 -  الخاصية "Comments"، التي يمكننا عرضها باستخدام حقل COMMENTS:
properties.comments = f"This is {properties.author}'s document about {properties.subject}"
builder.write('\nComments:\t"')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_COMMENTS, update_field=True)
builder.write('"')
# الخاصية المدمجة "Category" لا تحتوي على حقل يمكنه عرض قيمتها.
properties.category = 'My category'
# يمكننا تعيين عدة كلمات مفتاحية لمستند عن طريق فصل قيمة السلسلة للخاصية "Keywords" بفواصل منقوطة.
properties.keywords = 'Tag 1; Tag 2; Tag 3'
# يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على هذه الخصائص في "Properties" -> "Details".
# الخاصية المدمجة "Author" موجودة في مجموعة "Origin"، والبقية في مجموعة "Description".
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.Description.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

