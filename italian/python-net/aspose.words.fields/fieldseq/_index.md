---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /it/python-net/aspose.words.fields/fieldseq/
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
# Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
# Ogni voce contiene il paragrafo che include il campo SEQ e il numero di pagina in cui il campo appare.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# I campi SEQ mostrano un conteggio che si incrementa ad ogni campo SEQ.
# Questi campi mantengono anche conteggi separati per ogni sequenza nominata univocamente
# identificata dalla proprietà "SequenceIdentifier" del campo SEQ.
# Usa la proprietà "TableOfFiguresLabel" per nominare una sequenza principale per il TOC.
# Ora, questo TOC creerà voci solo dai campi SEQ il cui "SequenceIdentifier" è impostato su "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Possiamo nominare un'altra sequenza di campi SEQ nella proprietà "PrefixedSequenceIdentifier".
# I campi SEQ di questa sequenza prefissa non creeranno voci nel TOC.
# Ogni voce del TOC creata da un campo SEQ di sequenza principale ora mostrerà anche il conteggio che
# la sequenza prefisso è attualmente su nel campo SEQ della sequenza primaria che ha creato la voce.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Ogni voce del TOC mostrerà il conteggio della sequenza prefisso immediatamente a sinistra
# del numero di pagina su cui appare il campo SEQ della sequenza principale.
# Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Ci sono due modi per usare i campi SEQ per popolare questo TOC.
# 1 -  Inserimento di un campo SEQ che appartiene alla sequenza prefisso del TOC:
# Questo campo incrementerà il conteggio della sequenza SEQ per la "PrefixSequence" di 1.
# Poiché questo campo non appartiene alla sequenza principale identificata
# dalla proprietà "TableOfFiguresLabel" del TOC, non apparirà come voce.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Inserimento di un campo SEQ che appartiene alla sequenza principale del TOC:
# Questo campo SEQ creerà una voce nel TOC.
# La voce del TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero di pagina su cui appare.
# Questa voce mostrerà anche il conteggio a cui è attualmente la sequenza prefisso,
# separato dal numero di pagina dal valore nella proprietà SeqenceSeparator del TOC.
# Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale è a pagina 2,
# e il separatore è ">", quindi la voce mostrerà "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Inserisci una pagina, avanza la sequenza prefisso di 2 e inserisci un campo SEQ per creare una voce del TOC successivamente.
# La sequenza prefisso è ora a 2, e il campo SEQ della sequenza principale è a pagina 3,
# quindi la voce del TOC mostrerà "2>3" nel suo conteggio di pagina.
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
# I campi SEQ mostrano un conteggio che si incrementa ad ogni campo SEQ.
# Questi campi mantengono anche conteggi separati per ogni sequenza nominata univocamente
# identificata dalla proprietà "SequenceIdentifier" del campo SEQ.
# Inserisci un campo SEQ che mostrerà il valore di conteggio corrente di "MySequence",
# dopo aver usato la proprietà "ResetNumber" per impostarlo a 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Visualizza il numero successivo in questa sequenza con un altro campo SEQ.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Inserisci un'intestazione di livello 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Inserisci un altro campo SEQ dalla stessa sequenza e configurarlo per azzerare il conteggio a ogni intestazione con 1.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# L'intestazione sopra è un'intestazione di livello 1, quindi il conteggio per questa sequenza è azzerato a 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Passa al numero successivo di questa sequenza.
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

* module [aspose.words.fields](../)
* class [Field](../field/)

