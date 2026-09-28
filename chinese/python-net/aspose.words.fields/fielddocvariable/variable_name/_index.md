---
title: FieldDocVariable.variable_name property
linktitle: variable_name property
articleTitle: variable_name property
second_title: Aspose.Words for Python
description: "FieldDocVariable.variable_name property. Gets or sets the name of the document variable to retrieve."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fielddocvariable/variable_name/
---

## FieldDocVariable.variable_name property

Gets or sets the name of the document variable to retrieve.


```python
@property
def variable_name(self) -> str:
    ...

@variable_name.setter
def variable_name(self, value: str):
    ...

```

### Examples

Shows how to use DOCPROPERTY fields to display document properties and variables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 以下是使用 DOCPROPERTY 字段的两种方式。
# 1 - 显示内置属性：
# 为 "Category" 内置属性设置自定义值，然后插入引用该属性的 DOCPROPERTY 字段。
doc.built_in_document_properties.category = 'My category'
field_doc_property = builder.insert_field(field_code=' DOCPROPERTY Category ').as_field_doc_property()
field_doc_property.update()
self.assertEqual(' DOCPROPERTY Category ', field_doc_property.get_field_code())
self.assertEqual('My category', field_doc_property.result)
builder.insert_paragraph()
# 2 - 显示自定义文档变量：
# 定义自定义变量，然后使用 DOCPROPERTY 字段引用该变量。
self.assertEqual(0, doc.variables.count)
doc.variables.add('My variable', "My variable's value")
field_doc_variable = builder.insert_field(field_type=fields.FieldType.FIELD_DOC_VARIABLE, update_field=True).as_field_doc_variable()
field_doc_variable.variable_name = 'My variable'
field_doc_variable.update()
self.assertEqual(' DOCVARIABLE  "My variable"', field_doc_variable.get_field_code())
self.assertEqual("My variable's value", field_doc_variable.result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.DOCPROPERTY.DOCVARIABLE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldDocVariable](../)

