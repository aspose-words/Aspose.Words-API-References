---
title: FieldToc.sequence_separator property
linktitle: sequence_separator property
articleTitle: sequence_separator property
second_title: Aspose.Words for Python
description: "FieldToc.sequence_separator property. Gets or sets the character sequence that is used to separate sequence numbers and page numbers."
type: docs
weight: 150
url: /de/python-net/aspose.words.fields/fieldtoc/sequence_separator/
---

## FieldToc.sequence_separator property

Gets or sets the character sequence that is used to separate sequence numbers and page numbers.


```python
@property
def sequence_separator(self) -> str:
    ...

@sequence_separator.setter
def sequence_separator(self, value: str):
    ...

```

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

