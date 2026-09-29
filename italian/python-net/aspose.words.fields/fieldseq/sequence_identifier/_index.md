---
title: FieldSeq.sequence_identifier property
linktitle: sequence_identifier property
articleTitle: sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldSeq.sequence_identifier property. Gets or sets the name assigned to the series of items that are to be numbered."
type: docs
weight: 60
url: /it/python-net/aspose.words.fields/fieldseq/sequence_identifier/
---

## FieldSeq.sequence_identifier property

Gets or sets the name assigned to the series of items that are to be numbered.


```python
@property
def sequence_identifier(self) -> str:
    ...

@sequence_identifier.setter
def sequence_identifier(self, value: str):
    ...

```

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

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

