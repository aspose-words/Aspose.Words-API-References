---
title: FieldIndex.sequence_name property
linktitle: sequence_name property
articleTitle: sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_name property. Gets or sets the name of a sequence whose number is included with the page number."
type: docs
weight: 150
url: /es/python-net/aspose.words.fields/fieldindex/sequence_name/
---

## FieldIndex.sequence_name property

Gets or sets the name of a sequence whose number is included with the page number.


```python
@property
def sequence_name(self) -> str:
    ...

@sequence_name.setter
def sequence_name(self, value: str):
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
# Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
# y el número de la página que contiene el campo XE a la derecha.
# Si los campos XE tienen el mismo valor en su propiedad "Text",
# el campo INDEX los agrupará en una sola entrada.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# En la propiedad SequenceName, nombre una secuencia de campo SEQ. Cada entrada de este campo INDEX ahora también mostrará
# el número en el que está el recuento de la secuencia en la ubicación del campo XE que creó esta entrada.
index.sequence_name = 'MySequence'
# Establezca texto que rodeará la secuencia y los números de página para explicar su significado al usuario.
# Una entrada creada con esta configuración mostrará algo como "MySequence at 1 on page 1" en su número de página.
# PageNumberSeparator y SequenceSeparator no pueden ser más largos de 15 caracteres.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
# Estos campos también mantienen recuentos separados para cada secuencia nombrada única
# identificada por la propiedad "SequenceIdentifier" del campo SEQ.
# Inserte un campo SEQ que mueva la secuencia "MySequence" a 1.
# Este campo no es diferente del texto normal del documento. No aparecerá en la tabla de contenido de un campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Inserte un campo XE que creará una entrada en el campo INDEX.
# Dado que "MySequence" está en 1 y este campo XE está en la página 2, junto con los separadores personalizados que definimos arriba,
# la entrada INDEX de este campo mostrará "Cat" en el lado izquierdo, y "MySequence at 1 on page 2" en el derecho.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Inserte un salto de página y use campos SEQ para avanzar "MySequence" a 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Inserte un campo XE con la misma propiedad Text que el anterior.
# La entrada INDEX agrupará los campos XE con valores coincidentes en la propiedad "Text"
# en una sola entrada en lugar de crear una entrada para cada campo XE.
# Dado que estamos en la página 2 con "MySequence" en 3, ", 3 on page 3" se añadirá a la misma entrada INDEX que arriba.
# La porción del número de página de esa entrada INDEX ahora mostrará "MySequence at 1 on page 2, 3 on page 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Inserte un campo XE con un valor de propiedad Text nuevo y único.
# Esto añadirá una nueva entrada, con MySequence en 3 en la página 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

