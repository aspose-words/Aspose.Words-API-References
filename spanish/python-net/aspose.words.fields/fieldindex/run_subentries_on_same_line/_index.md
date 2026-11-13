---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /es/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
# y el número de la página que contiene el campo XE a la derecha.
# La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
# en una sola entrada en lugar de crear una entrada para cada campo XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# Campos XE que tienen una propiedad Text cuyo valor se convierte en el encabezado de la entrada INDEX.
# Si este valor contiene dos segmentos de cadena separados por dos puntos (el delimitador :) que la entrada INDEX tratará,
# el primer segmento es el encabezado, y el segundo segmento se convertirá en el subencabezado.
# El campo INDEX primero agrupa las entradas alfabéticamente, luego, si hay varios campos XE con el mismo
# encabezados, el campo INDEX subdividirá aún más por los valores de esos encabezados.
# Puede haber múltiples capas de subagrupación, dependiendo de cuántas veces
# las propiedades Text de los campos XE se segmenten de esta manera.
# Por defecto, un grupo de entradas de campo INDEX creará una nueva línea para cada subencabezado dentro de este grupo.
# Podemos establecer la bandera RunSubentriesOnSameLine a true para mantener el encabezado,
# y cada subencabezado del grupo en una sola línea, lo que hará que el campo INDEX sea más compacto.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# Inserte dos campos XE, cada uno en una nueva página, y con el mismo encabezado llamado "Heading 1",
# que el campo INDEX usará para agruparlos.
# Si RunSubentriesOnSameLine es false, entonces la tabla INDEX creará tres líneas:
# una línea para el encabezado de agrupación "Heading 1", y una línea más para cada subencabezado.
# Si RunSubentriesOnSameLine es true, entonces la tabla INDEX creará una línea única
# entrada que abarca el encabezado y cada subencabezado.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

