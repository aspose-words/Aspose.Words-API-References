---
title: FieldIndex.has_page_number_separator property
linktitle: has_page_number_separator property
articleTitle: has_page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.has_page_number_separator property. Gets a value indicating whether a page number separator is overridden through the field's code."
type: docs
weight: 50
url: /es/python-net/aspose.words.fields/fieldindex/has_page_number_separator/
---

## FieldIndex.has_page_number_separator property

Gets a value indicating whether a page number separator is overridden through the field's code.


```python
@property
def has_page_number_separator(self) -> bool:
    ...

```

### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
# y el número de la página que contiene el campo XE a la derecha.
# La entrada INDEX agrupará los campos XE con valores coincidentes en la propiedad "Text"
# en una sola entrada en lugar de crear una entrada para cada campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Si nuestro campo INDEX tiene una entrada para un grupo de campos XE,
# esta entrada mostrará el número de cada página que contiene un campo XE que pertenece a este grupo.
# Podemos establecer separadores personalizados para personalizar la apariencia de estos números de página.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# Después de insertar estos campos XE, el campo INDEX mostrará "Primera entrada, en la(s) página(s) 2 & 3 & 4".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
self.assertEqual(' XE  "First entry"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageNumberList.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

