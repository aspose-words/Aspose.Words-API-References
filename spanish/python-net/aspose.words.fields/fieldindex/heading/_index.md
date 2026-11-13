---
title: FieldIndex.heading property
linktitle: heading property
articleTitle: heading property
second_title: Aspose.Words for Python
description: "FieldIndex.heading property. Gets or sets a heading that appears at the start of each set of entries for any given letter."
type: docs
weight: 70
url: /es/python-net/aspose.words.fields/fieldindex/heading/
---

## FieldIndex.heading property

Gets or sets a heading that appears at the start of each set of entries for any given letter.


```python
@property
def heading(self) -> str:
    ...

@heading.setter
def heading(self, value: str):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
# y el número de la página que contiene el campo XE a la derecha.
# Si los campos XE tienen el mismo valor en su propiedad "Text",
# el campo INDEX los agrupará en una sola entrada.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Establecer el valor de esta propiedad a "A" agrupará todas las entradas por su primera letra,
# y colocará esa letra en mayúsculas sobre cada grupo.
index.heading = 'A'
# Configure la tabla creada por el campo INDEX para que abarque 2 columnas.
index.number_of_columns = '2'
# Configure cualquier entrada con letras iniciales fuera del rango de caracteres "a-c" para que se omita.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Los siguientes dos campos XE aparecerán bajo el encabezado "A",
# con sus respectivos estilos de texto también aplicados a sus números de página.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Los dos siguientes campos XE estarán bajo los encabezados "B" y "C" en el índice de contenidos del campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# Los campos INDEX ordenan todas las entradas alfabéticamente, por lo que esta entrada aparecerá bajo "A" junto a las otras dos.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Esta entrada no aparecerá porque comienza con la letra "D",
# que está fuera del rango de caracteres "a-c" que define la propiedad LetterRange del campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

