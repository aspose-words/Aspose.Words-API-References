---
title: FieldToc.prefixed_sequence_identifier property
linktitle: prefixed_sequence_identifier property
articleTitle: prefixed_sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.prefixed_sequence_identifier property. Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number."
type: docs
weight: 120
url: /it/python-net/aspose.words.fields/fieldtoc/prefixed_sequence_identifier/
---

## FieldToc.prefixed_sequence_identifier property

Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number.


```python
@property
def prefixed_sequence_identifier(self) -> str:
    ...

@prefixed_sequence_identifier.setter
def prefixed_sequence_identifier(self, value: str):
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

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

