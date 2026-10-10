---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /de/python-net/aspose.words.fields/fieldseq/
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
# Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
# Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält, sowie die Seitennummer, auf der das Feld erscheint.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Verwenden Sie die "TableOfFiguresLabel"-Eigenschaft, um eine Hauptsequenz für das TOC zu benennen.
# Jetzt wird dieses TOC nur Einträge aus SEQ-Feldern erstellen, deren "SequenceIdentifier" auf "MySequence" gesetzt ist.
field_toc.table_of_figures_label = 'MySequence'
# Wir können eine weitere SEQ-Feldsequenz in der "PrefixedSequenceIdentifier"-Eigenschaft benennen.
# SEQ-Felder aus dieser Präfixsequenz werden keine TOC-Einträge erzeugen.
# Jeder aus einem Hauptsequenz-SEQ-Feld erstellte TOC-Eintrag wird nun ebenfalls die Zählung anzeigen, die
# Die Präfixsequenz befindet sich derzeit im primären Sequenz‑SEQ‑Feld, das den Eintrag erzeugt hat.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Jeder TOC‑Eintrag zeigt die Präfixsequenz‑Zählung sofort links davon an
# der Seitenzahl, auf der das Hauptsequenz‑SEQ‑Feld erscheint.
# Wir können einen benutzerdefinierten Trennzeichen angeben, das zwischen diesen beiden Zahlen erscheint.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Es gibt zwei Möglichkeiten, SEQ‑Felder zu verwenden, um dieses TOC zu füllen.
# 1 -  Einfügen eines SEQ‑Feldes, das zur Präfixsequenz des TOC gehört:
# Dieses Feld erhöht die SEQ‑Sequenz‑Zählung für "PrefixSequence" um 1.
# Da dieses Feld nicht zur identifizierten Hauptsequenz gehört
# durch die "TableOfFiguresLabel"‑Eigenschaft des TOC, wird es nicht als Eintrag erscheinen.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Einfügen eines SEQ‑Feldes, das zur Hauptsequenz des TOC gehört:
# Dieses SEQ‑Feld wird einen Eintrag im TOC erzeugen.
# Der TOC‑Eintrag enthält den Absatz, in dem das SEQ‑Feld steht, sowie die Seitenzahl, auf der es erscheint.
# Dieser Eintrag zeigt außerdem die aktuelle Zählung der Präfixsequenz an,
# getrennt von der Seitenzahl durch den Wert in der "SeqenceSeparator"‑Eigenschaft des TOC.
# Die Zählung von "PrefixSequence" ist 1, dieses Hauptsequenz‑SEQ‑Feld befindet sich auf Seite 2,
# und das Trennzeichen ist ">", sodass der Eintrag "1>2" anzeigt.
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Fügen Sie eine Seite ein, erhöhen Sie die Präfixsequenz um 2 und fügen Sie anschließend ein SEQ‑Feld ein, um einen TOC‑Eintrag zu erstellen.
# Die Präfixsequenz ist jetzt 2, und das Hauptsequenz‑SEQ‑Feld befindet sich auf Seite 3,
# so zeigt der TOC‑Eintrag "2>3" bei seiner Seitenzahl an.
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
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Fügen Sie ein SEQ‑Feld ein, das den aktuellen Zählwert von "MySequence" anzeigt,
# nachdem Sie die "ResetNumber"‑Eigenschaft verwendet haben, um sie auf 100 zu setzen.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Zeigen Sie die nächste Nummer in dieser Sequenz mit einem weiteren SEQ‑Feld an.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Fügen Sie eine Überschrift der Ebene 1 ein.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Fügen Sie ein weiteres SEQ‑Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass die Zählung bei jeder Überschrift mit 1 zurückgesetzt wird.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Die obige Überschrift ist eine Überschrift der Ebene 1, sodass die Zählung für diese Sequenz auf 1 zurückgesetzt wird.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Gehe zur nächsten Nummer dieser Sequenz.
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
# Ein TOC-Feld kann für jedes im Dokument gefundene SEQ-Feld einen Eintrag in seinem Inhaltsverzeichnis erstellen.
# Jeder Eintrag enthält den Absatz, der das SEQ-Feld enthält,
# und die Seitenzahl, auf der das Feld erscheint.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfiguriere dieses TOC-Feld so, dass es eine SequenceIdentifier-Eigenschaft mit dem Wert "MySequence" hat.
field_toc.table_of_figures_label = 'MySequence'
# Konfiguriere dieses TOC-Feld so, dass es nur SEQ-Felder übernimmt, die innerhalb der Grenzen eines Lesezeichens liegen
# mit dem Namen "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Füge ein SEQ-Feld ein, das einen Sequenzbezeichner hat, der dem TOC's
# TableOfFiguresLabel-Eigenschaft. Dieses Feld wird keinen Eintrag im TOC erzeugen, da es außerhalb ist
# der vom Lesezeichen "BookmarkName" festgelegten Grenzen.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Die Sequenz dieses SEQ-Feldes stimmt mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein und liegt innerhalb der Lesezeichen-Grenzen.
# Der Absatz, der dieses Feld enthält, wird im TOC als Eintrag angezeigt.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Die Sequenz dieses SEQ-Feldes stimmt nicht mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein,
# liegt jedoch innerhalb der Lesezeichen-Grenzen. Sein Absatz wird im TOC nicht als Eintrag angezeigt.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Die Sequenz dieses SEQ-Feldes stimmt mit der "TableOfFiguresLabel"-Eigenschaft des TOC überein und liegt innerhalb der Lesezeichen-Grenzen.
# Dieses Feld verweist außerdem auf ein anderes Lesezeichen. Der Inhalt dieses Lesezeichens erscheint im TOC-Eintrag für dieses SEQ-Feld.
# Das SEQ-Feld selbst wird den Inhalt dieses Lesezeichens nicht anzeigen.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Erstelle ein Lesezeichen mit Inhalt, das im TOC-Eintrag erscheint, weil das obige SEQ-Feld darauf verweist.
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

