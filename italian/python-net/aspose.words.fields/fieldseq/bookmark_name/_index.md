---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fieldseq/bookmark_name/
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
# Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
# Ogni voce contiene il paragrafo che contiene il campo SEQ,
# e il numero della pagina in cui appare il campo.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Configura questo campo TOC affinché abbia una proprietà SequenceIdentifier con valore "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Configura questo campo TOC per acquisire solo i campi SEQ che si trovano entro i limiti di un segnalibro
# denominato "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# I campi SEQ mostrano un conteggio che si incrementa ad ogni campo SEQ.
# Questi campi mantengono anche conteggi separati per ogni sequenza nominata univocamente
# identificata dalla proprietà "SequenceIdentifier" del campo SEQ.
# Inserisci un campo SEQ che abbia un identificatore di sequenza che corrisponda a quello del TOC
# proprietà TableOfFiguresLabel. Questo campo non creerà una voce nel TOC poiché è al di fuori
# dei limiti del segnalibro designati da "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è entro i limiti del segnalibro.
# Il paragrafo che contiene questo campo apparirà nel TOC come voce.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# La sequenza di questo campo SEQ non corrisponde alla proprietà "TableOfFiguresLabel" del TOC,
# ed è entro i limiti del segnalibro. Il suo paragrafo non apparirà nel TOC come voce.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è entro i limiti del segnalibro.
# Questo campo fa anche riferimento a un altro segnalibro. Il contenuto di quel segnalibro apparirà nella voce del TOC per questo campo SEQ.
# Il campo SEQ stesso non visualizzerà il contenuto di quel segnalibro.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Crea un segnalibro con contenuti che appariranno nella voce del TOC a causa del riferimento del campo SEQ sopra.
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

