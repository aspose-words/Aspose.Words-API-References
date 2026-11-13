---
title: FieldTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldTitle.text property. Gets or sets the text of the title."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldtitle/text/
---

## FieldTitle.text property

Gets or sets the text of the title.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to use the TITLE field.

```python
doc = aw.Document()
# Establezca un valor para la propiedad incorporada del documento "Title".
doc.built_in_document_properties.title = 'My Title'
# Podemos usar el campo TITLE para mostrar el valor de esta propiedad en el documento.
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=False).as_field_title()
field.update()
self.assertEqual(' TITLE ', field.get_field_code())
self.assertEqual('My Title', field.result)
# Estableciendo un valor para la propiedad Text del campo,
# y luego actualizar el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TITLE, update_field=False).as_field_title()
field.text = 'My New Title'
field.update()
self.assertEqual(' TITLE  "My New Title"', field.get_field_code())
self.assertEqual('My New Title', field.result)
self.assertEqual('My New Title', doc.built_in_document_properties.title)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TITLE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTitle](../)

