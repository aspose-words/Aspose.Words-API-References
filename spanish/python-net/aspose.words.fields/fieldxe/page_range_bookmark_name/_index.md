---
title: FieldXE.page_range_bookmark_name property
linktitle: page_range_bookmark_name property
articleTitle: page_range_bookmark_name property
second_title: Aspose.Words for Python
description: "FieldXE.page_range_bookmark_name property. Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number."
type: docs
weight: 60
url: /es/python-net/aspose.words.fields/fieldxe/page_range_bookmark_name/
---

## FieldXE.page_range_bookmark_name property

Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number.


```python
@property
def page_range_bookmark_name(self) -> str:
    ...

@page_range_bookmark_name.setter
def page_range_bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
# y el número de la página que contiene el campo XE a la derecha.
# La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
# en una sola entrada en lugar de crear una entrada para cada campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Para las entradas INDEX que muestran rangos de páginas, podemos especificar una cadena separadora
# que aparecerá entre el número de la primera página y el número de la última.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Si un campo XE nombra un marcador usando la propiedad PageRangeBookmarkName,
# su entrada INDEX mostrará el rango de páginas que abarca el marcador
# en lugar del número de la página que contiene el campo XE.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Inserte un marcador que comience en la página 3 y termine en la página 5.
# La entrada INDEX para el campo XE que hace referencia a este marcador mostrará este rango de páginas.
# En nuestra tabla, la entrada INDEX mostrará "My entry, on page(s) 3 to 5".
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MyBookmark')
builder.write('Start of MyBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('End of MyBookmark')
builder.end_bookmark('MyBookmark')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageRangeBookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

