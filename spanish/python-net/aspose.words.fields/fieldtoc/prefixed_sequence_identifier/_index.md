---
title: FieldToc.prefixed_sequence_identifier property
linktitle: prefixed_sequence_identifier property
articleTitle: prefixed_sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.prefixed_sequence_identifier property. Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number."
type: docs
weight: 120
url: /es/python-net/aspose.words.fields/fieldtoc/prefixed_sequence_identifier/
---

## FieldToc.prefixed_sequence_identifier property

Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number.


```python
@property
def prefixed_sequence_identifier(self) -> str:
    ...

@prefixed_sequence_identifier.setter
def prefixed_sequence_identifier(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Un campo TOC puede crear una entrada en su tabla de contenido por cada campo SEQ encontrado en el documento.
# Cada entrada contiene el párrafo que incluye el campo SEQ y el número de página donde aparece el campo.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
# Estos campos también mantienen recuentos separados para cada secuencia nombrada única
# identificada por la propiedad "SequenceIdentifier" del campo SEQ.
# Utilice la propiedad "TableOfFiguresLabel" para nombrar una secuencia principal para el TOC.
# Ahora, este TOC solo creará entradas a partir de campos SEQ cuya "SequenceIdentifier" esté establecida en "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Podemos nombrar otra secuencia de campos SEQ en la propiedad "PrefixedSequenceIdentifier".
# Los campos SEQ de esta secuencia de prefijo no crearán entradas en el TOC.
# Cada entrada del TOC creada a partir de un campo SEQ de secuencia principal ahora también mostrará el recuento que
# la secuencia de prefijo está actualmente en el campo SEQ de la secuencia primaria que creó la entrada.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Cada entrada del TOC mostrará el recuento de la secuencia de prefijo inmediatamente a la izquierda
# del número de página en el que aparece el campo SEQ de la secuencia principal.
# Podemos especificar un separador personalizado que aparecerá entre estos dos números.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Hay dos formas de usar campos SEQ para rellenar este TOC.
# 1 -  Insertar un campo SEQ que pertenece a la secuencia de prefijo del TOC:
# Este campo incrementará el recuento de la secuencia SEQ para "PrefixSequence" en 1.
# Dado que este campo no pertenece a la secuencia principal identificada
# por la propiedad "TableOfFiguresLabel" del TOC, no aparecerá como una entrada.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Insertar un campo SEQ que pertenece a la secuencia principal del TOC:
# Este campo SEQ creará una entrada en el TOC.
# La entrada del TOC contendrá el párrafo en el que se encuentra el campo SEQ y el número de página en el que aparece.
# Esta entrada también mostrará el recuento en el que se encuentra actualmente la secuencia de prefijo,
# separado del número de página por el valor de la propiedad SeqenceSeparator del TOC.
# El recuento "PrefixSequence" está en 1, este campo SEQ de la secuencia principal está en la página 2,
# y el separador es ">", por lo que la entrada mostrará "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Inserte una página, avance la secuencia de prefijo en 2 y inserte un campo SEQ para crear una entrada del TOC después.
# La secuencia de prefijo está ahora en 2, y el campo SEQ de la secuencia principal está en la página 3,
# por lo que la entrada del TOC mostrará "2>3" en su recuento de página.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

