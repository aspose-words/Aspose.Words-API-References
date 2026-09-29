---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldseq/bookmark_name/
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
# Ett TOC-fält kan skapa en post i sin innehållsförteckning för varje SEQ-fält som finns i dokumentet.
# Varje post innehåller stycket som innehåller SEQ-fältet,
# och sidnumret där fältet visas.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfigurera detta TOC-fält så att det har egenskapen SequenceIdentifier med värdet "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Konfigurera detta TOC-fält så att det bara plockar upp SEQ-fält som ligger inom gränserna för ett bokmärke
# med namnet "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Infoga ett SEQ-fält som har en sekvensidentifierare som matchar TOC:ens
# TableOfFiguresLabel-egenskapen. Detta fält kommer inte att skapa en post i TOC eftersom det är utanför
# bokmärkesgränserna som anges av "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# Detta SEQ-fälts sekvens matchar TOC:ens "TableOfFiguresLabel"-egenskap och ligger inom bokmärkesgränserna.
# Stycket som innehåller detta fält kommer att visas i TOC som en post.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# Detta SEQ-fälts sekvens matchar inte TOC:ens "TableOfFiguresLabel"-egenskap,
# och ligger inom bokmärkesgränserna. Dess stycke kommer inte att visas i TOC som en post.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# Detta SEQ-fälts sekvens matchar TOC:ens "TableOfFiguresLabel"-egenskap och ligger inom bokmärkesgränserna.
# Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i TOC-posten för detta SEQ-fält.
# SEQ-fältet självt kommer inte att visa innehållet i det bokmärket.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Skapa ett bokmärke med innehåll som kommer att visas i TOC-posten på grund av att ovanstående SEQ-fält refererar till det.
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

