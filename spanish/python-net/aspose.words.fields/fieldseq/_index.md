---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /es/python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
# Estos campos también mantienen recuentos separados para cada secuencia nombrada única
# identificada por la propiedad "SequenceIdentifier" del campo SEQ.
# Inserte un campo SEQ que mostrará el valor actual del recuento de "MySequence",
# después de usar la propiedad "ResetNumber" para establecerlo en 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Muestre el siguiente número en esta secuencia con otro campo SEQ.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Inserte un encabezado de nivel 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Inserte otro campo SEQ de la misma secuencia y configúrelo para restablecer el recuento a 1 en cada encabezado.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# El encabezado anterior es un encabezado de nivel 1, por lo que el recuento de esta secuencia se restablece a 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Mueva al siguiente número de esta secuencia.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Un campo TOC puede crear una entrada en su tabla de contenido por cada campo SEQ encontrado en el documento.
# Cada entrada contiene el párrafo que contiene el campo SEQ,
# y el número de la página en la que aparece el campo.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Configure este campo TOC para que tenga una propiedad SequenceIdentifier con un valor de "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Configure este campo TOC para que solo capture campos SEQ que estén dentro de los límites de un marcador
# llamado "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
# Estos campos también mantienen recuentos separados para cada secuencia nombrada única
# identificada por la propiedad "SequenceIdentifier" del campo SEQ.
# Inserte un campo SEQ que tenga un identificador de secuencia que coincida con el TOC's
# propiedad TableOfFiguresLabel. Este campo no creará una entrada en el TOC ya que está fuera
# de los límites del marcador designados por "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
# El párrafo que contiene este campo aparecerá en el TOC como una entrada.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# La secuencia de este campo SEQ no coincide con la propiedad "TableOfFiguresLabel" del TOC,
# y está dentro de los límites del marcador. Su párrafo no aparecerá en el TOC como una entrada.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
# Este campo también hace referencia a otro marcador. El contenido de ese marcador aparecerá en la entrada del TOC para este campo SEQ.
# El propio campo SEQ no mostrará el contenido de ese marcador.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Cree un marcador con contenido que aparecerá en la entrada del TOC debido a que el campo SEQ anterior lo referencia.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

