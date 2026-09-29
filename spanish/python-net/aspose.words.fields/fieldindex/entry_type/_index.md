---
title: FieldIndex.entry_type property
linktitle: entry_type property
articleTitle: entry_type property
second_title: Aspose.Words for Python
description: "FieldIndex.entry_type property. Gets or sets an index entry type used to build the index."
type: docs
weight: 40
url: /es/python-net/aspose.words.fields/fieldindex/entry_type/
---

## FieldIndex.entry_type property

Gets or sets an index entry type used to build the index.


```python
@property
def entry_type(self) -> str:
    ...

@entry_type.setter
def entry_type(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo
# y la página que contiene el campo XE a la derecha.
# Si los campos XE tienen el mismo valor en su propiedad "Text",
# el campo INDEX los agrupará en una sola entrada.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Configure el campo INDEX para que solo muestre los campos XE que estén dentro de los límites
# de un marcador llamado "MainBookmark", y cuyas propiedades "EntryType" tengan un valor de "A".
# Para los campos INDEX y XE, la propiedad "EntryType" solo utiliza el primer carácter de su valor de cadena.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# En una página nueva, inicie el marcador con un nombre que coincida con el valor
# de la propiedad "BookmarkName" del campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# El campo INDEX capturará esta entrada porque está dentro del marcador,
# y su tipo de entrada también coincide con el tipo de entrada del campo INDEX.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Inserte un campo XE que no aparecerá en el INDEX porque los tipos de entrada no coinciden.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Finalice el marcador e inserte un campo XE después.
# Es del mismo tipo que el campo INDEX, pero no aparecerá
# ya que está fuera de los límites del marcador.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

