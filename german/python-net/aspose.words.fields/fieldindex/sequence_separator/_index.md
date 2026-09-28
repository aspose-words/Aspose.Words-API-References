---
title: FieldIndex.sequence_separator property
linktitle: sequence_separator property
articleTitle: sequence_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_separator property. Gets or sets the character sequence that is used to separate sequence numbers and page numbers."
type: docs
weight: 160
url: /de/python-net/aspose.words.fields/fieldindex/sequence_separator/
---

## FieldIndex.sequence_separator property

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

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
# Jeder Eintrag zeigt den Wert der Text‑Eigenschaft des XE‑Feldes auf der linken Seite an,
# und die Seitenzahl, die das XE‑Feld enthält, auf der rechten Seite.
# Wenn die XE-Felder denselben Wert in ihrer "Text"-Eigenschaft haben,
# wird das INDEX-Feld sie zu einem Eintrag zusammenfassen.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Im SequenceName‑Eigenschaft geben Sie eine SEQ‑Feldsequenz an. Jeder Eintrag dieses INDEX-Feldes wird nun außerdem anzeigen
# die Nummer, bei der der Sequenzzähler am Standort des XE-Feldes steht, das diesen Eintrag erstellt hat.
index.sequence_name = 'MySequence'
# Legen Sie Text fest, der um die Sequenz und Seitenzahlen herum angezeigt wird, um deren Bedeutung dem Benutzer zu erklären.
# Ein mit dieser Konfiguration erstellter Eintrag zeigt etwa "MySequence bei 1 auf Seite 1" bei seiner Seitenzahl an.
# PageNumberSeparator und SequenceSeparator dürfen nicht länger als 15 Zeichen sein.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Fügen Sie ein SEQ-Feld ein, das die "MySequence"‑Sequenz auf 1 verschiebt.
# Dieses Feld unterscheidet sich nicht von normalem Dokumenttext. Es wird nicht im Inhaltsverzeichnis eines INDEX-Feldes erscheinen.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Fügen Sie ein XE-Feld ein, das einen Eintrag im INDEX-Feld erzeugt.
# Da "MySequence" bei 1 steht und dieses XE-Feld auf Seite 2 ist, zusammen mit den oben definierten benutzerdefinierten Trennzeichen,
# wird der INDEX‑Eintrag dieses Feldes "Cat" auf der linken Seite und "MySequence bei 1 auf Seite 2" auf der rechten Seite anzeigen.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Fügen Sie einen Seitenumbruch ein und verwenden Sie SEQ-Felder, um "MySequence" auf 3 zu erhöhen.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Fügen Sie ein XE-Feld mit derselben Text‑Eigenschaft wie das obige ein.
# Der INDEX-Eintrag wird XE-Felder mit übereinstimmenden Werten in der "Text"-Eigenschaft gruppieren
# zu einem einzigen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
# Da wir auf Seite 2 mit "MySequence" bei 3 sind, wird ", 3 auf Seite 3" an denselben INDEX‑Eintrag wie oben angehängt.
# Der Seitenzahl‑Teil dieses INDEX‑Eintrags wird nun "MySequence bei 1 auf Seite 2, 3 auf Seite 3" anzeigen.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Fügen Sie ein XE-Feld mit einem neuen und eindeutigen Text‑Eigenschaftswert ein.
# Dies wird einen neuen Eintrag hinzufügen, mit MySequence bei 3 auf Seite 4.
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

