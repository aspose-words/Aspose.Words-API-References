---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

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

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

