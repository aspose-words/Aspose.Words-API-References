---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fields/fieldseq/bookmark_name/
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
# Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
# Chaque entrée contient le paragraphe qui contient le champ SEQ,
# et le numéro de la page où le champ apparaît.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Configurez ce champ TOC pour qu'il possède une propriété SequenceIdentifier avec la valeur "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Configurez ce champ TOC pour ne récupérer que les champs SEQ qui se trouvent à l'intérieur des limites d'un signet
# nommé "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Insérez un champ SEQ dont l'identifiant de séquence correspond à celui du TOC
# propriété TableOfFiguresLabel. Ce champ ne créera pas d'entrée dans le TOC car il est en dehors
# des limites du signet désigné par "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
# Le paragraphe contenant ce champ apparaîtra dans le TOC comme une entrée.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# La séquence de ce champ SEQ ne correspond pas à la propriété "TableOfFiguresLabel" du TOC,
# et se trouve à l'intérieur des limites du signet. Son paragraphe n'apparaîtra pas dans le TOC comme une entrée.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# La séquence de ce champ SEQ correspond à la propriété "TableOfFiguresLabel" du TOC et se trouve à l'intérieur des limites du signet.
# Ce champ fait également référence à un autre signet. Le contenu de ce signet apparaîtra dans l'entrée du TOC pour ce champ SEQ.
# Le champ SEQ lui‑-même n'affichera pas le contenu de ce signet.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Créez un signet avec un contenu qui apparaîtra dans l'entrée du TOC en raison du champ SEQ ci‑dessus qui le référence.
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

