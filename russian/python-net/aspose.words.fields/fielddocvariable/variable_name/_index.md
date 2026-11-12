---
title: FieldDocVariable.variable_name property
linktitle: variable_name property
articleTitle: variable_name property
second_title: Aspose.Words for Python
description: "FieldDocVariable.variable_name property. Gets or sets the name of the document variable to retrieve."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fielddocvariable/variable_name/
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
# Ниже представлены два способа использования полей DOCPROPERTY.
# 1 -  Отобразить встроенное свойство:
# Установите пользовательское значение для встроенного свойства "Category", затем вставьте поле DOCPROPERTY, которое ссылается на него.
doc.built_in_document_properties.category = 'My category'
field_doc_property = builder.insert_field(field_code=' DOCPROPERTY Category ').as_field_doc_property()
field_doc_property.update()
self.assertEqual(' DOCPROPERTY Category ', field_doc_property.get_field_code())
self.assertEqual('My category', field_doc_property.result)
builder.insert_paragraph()
# 2 -  Отобразить пользовательскую переменную документа:
# Определите пользовательскую переменную, затем сослаться на эту переменную с помощью поля DOCPROPERTY.
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

