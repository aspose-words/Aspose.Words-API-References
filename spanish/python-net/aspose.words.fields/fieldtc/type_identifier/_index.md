---
title: FieldTC.type_identifier property
linktitle: type_identifier property
articleTitle: type_identifier property
second_title: Aspose.Words for Python
description: "FieldTC.type_identifier property. Gets or sets a type identifier for this field (which is typically a letter)."
type: docs
weight: 50
url: /es/python-net/aspose.words.fields/fieldtc/type_identifier/
---

## FieldTC.type_identifier property

Gets or sets a type identifier for this field (which is typically a letter).


```python
@property
def type_identifier(self) -> str:
    ...

@type_identifier.setter
def type_identifier(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte un campo TOC, que compilará todos los campos TC en una tabla de contenido.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Configure el campo para que solo capture entradas TC del tipo "A" y un nivel de entrada entre 1 y 3.
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# Estas dos entradas aparecerán en la tabla.
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# Esta entrada se omitirá de la tabla porque tiene un tipo diferente de "A".
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# Esta entrada se omitirá de la tabla porque tiene un nivel de entrada fuera del rango 1-3.
self.insert_toc_entry(builder, 'TC field 4', 'A', '5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TC.docx')
```

Shows how to insert a TOC field, and filter which TC fields end up as entries (InsertTocEntry).

```python
def insert_toc_entry(self, builder, text, type_identifier, entry_level):
    field_tc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC_ENTRY, update_field=True).as_field_tc()
    field_tc.omit_page_number = True
    field_tc.text = text
    field_tc.type_identifier = type_identifier
    field_tc.entry_level = entry_level
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTC](../)

