---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /fr/python-net/aspose.words.fields/fieldseq/
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
# Un champ TOC peut créer une entrée dans sa table des matières pour chaque champ SEQ trouvé dans le document.
# Chaque entrée contient le paragraphe qui inclut le champ SEQ ainsi que le numéro de page où le champ apparaît.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Utilisez la propriété "TableOfFiguresLabel" pour nommer une séquence principale pour le TOC.
# Désormais, ce TOC ne créera des entrées qu'à partir des champs SEQ dont le "SequenceIdentifier" est défini sur "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Nous pouvons nommer une autre séquence de champ SEQ dans la propriété "PrefixedSequenceIdentifier".
# Les champs SEQ de cette séquence préfixée ne créeront pas d'entrées TOC.
# Chaque entrée TOC créée à partir d'un champ SEQ de séquence principale affichera désormais également le compteur qui
# la séquence de préfixe est actuellement sur le champ SEQ de séquence principale qui a créé l'entrée.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Chaque entrée du TOC affichera le compteur de séquence de préfixe immédiatement à gauche
# du numéro de page sur lequel le champ SEQ de séquence principale apparaît.
# Nous pouvons spécifier un séparateur personnalisé qui apparaîtra entre ces deux nombres.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Il existe deux façons d'utiliser les champs SEQ pour remplir ce TOC.
# 1 - Insertion d'un champ SEQ qui appartient à la séquence de préfixe du TOC :
# Ce champ incrémentera le compteur de séquence SEQ pour le "PrefixSequence" de 1.
# Puisque ce champ n'appartient pas à la séquence principale identifiée
# par la propriété "TableOfFiguresLabel" du TOC, il n'apparaîtra pas comme une entrée.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - Insertion d'un champ SEQ qui appartient à la séquence principale du TOC :
# Ce champ SEQ créera une entrée dans le TOC.
# L'entrée du TOC contiendra le paragraphe dans lequel se trouve le champ SEQ ainsi que le numéro de la page où il apparaît.
# Cette entrée affichera également le compteur actuel de la séquence de préfixe,
# séparé du numéro de page par la valeur de la propriété SeqenceSeparator du TOC.
# Le compteur "PrefixSequence" est à 1, ce champ SEQ de séquence principale est à la page 2,
# et le séparateur est ">", donc l'entrée affichera "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Insérez une page, avancez la séquence de préfixe de 2, puis insérez un champ SEQ pour créer une entrée TOC ensuite.
# La séquence de préfixe est maintenant à 2, et le champ SEQ de séquence principale est à la page 3,
# ainsi l'entrée du TOC affichera "2>3" dans son compteur de page.
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
# Les champs SEQ affichent un compteur qui s'incrémente à chaque champ SEQ.
# Ces champs maintiennent également des compteurs séparés pour chaque séquence nommée unique
# identifiée par la propriété "SequenceIdentifier" du champ SEQ.
# Insérez un champ SEQ qui affichera la valeur du compteur actuel de "MySequence",
# après avoir utilisé la propriété "ResetNumber" pour le définir à 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Affichez le nombre suivant de cette séquence avec un autre champ SEQ.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Insérez un titre de niveau 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Insérez un autre champ SEQ de la même séquence et configurez-le pour réinitialiser le compteur à chaque titre avec 1.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Le titre ci‑dessus est un titre de niveau 1, donc le compteur de cette séquence est réinitialisé à 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Passez au nombre suivant de cette séquence.
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

* module [aspose.words.fields](../)
* class [Field](../field/)

