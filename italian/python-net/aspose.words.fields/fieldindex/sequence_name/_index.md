---
title: FieldIndex.sequence_name property
linktitle: sequence_name property
articleTitle: sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_name property. Gets or sets the name of a sequence whose number is included with the page number."
type: docs
weight: 150
url: /it/python-net/aspose.words.fields/fieldindex/sequence_name/
---

## FieldIndex.sequence_name property

Gets or sets the name of a sequence whose number is included with the page number.


```python
@property
def sequence_name(self) -> str:
    ...

@sequence_name.setter
def sequence_name(self, value: str):
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
# Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
# e il numero della pagina che contiene il campo XE sul lato destro.
# Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
# il campo INDEX li raggrupperà in un'unica voce.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Nella proprietà SequenceName, assegna un nome a una sequenza di campo SEQ. Ogni voce di questo campo INDEX ora visualizzerà anche
# il numero su cui si trova il conteggio della sequenza nella posizione del campo XE che ha creato questa voce.
index.sequence_name = 'MySequence'
# Imposta il testo che circonderà la sequenza e i numeri di pagina per spiegare il loro significato all'utente.
# Una voce creata con questa configurazione visualizzerà qualcosa come "MySequence a 1 su pagina 1" al suo numero di pagina.
# PageNumberSeparator e SequenceSeparator non possono superare i 15 caratteri.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# I campi SEQ mostrano un conteggio che si incrementa ad ogni campo SEQ.
# Questi campi mantengono anche conteggi separati per ogni sequenza nominata univocamente
# identificata dalla proprietà "SequenceIdentifier" del campo SEQ.
# Inserisci un campo SEQ che sposta la sequenza "MySequence" a 1.
# Questo campo non è diverso dal normale testo del documento. Non apparirà nella tabella dei contenuti di un campo INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Inserisci un campo XE che creerà una voce nel campo INDEX.
# Poiché "MySequence" è a 1 e questo campo XE è sulla pagina 2, insieme ai separatori personalizzati che abbiamo definito sopra,
# la voce INDEX di questo campo visualizzerà "Cat" sul lato sinistro e "MySequence a 1 su pagina 2" sul lato destro.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Inserisci un'interruzione di pagina e utilizza i campi SEQ per avanzare "MySequence" a 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Inserisci un campo XE con la stessa proprietà Text di quello sopra.
# La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Text"
# in una sola voce anziché creare una voce per ogni campo XE.
# Poiché siamo sulla pagina 2 con "MySequence" a 3, ", 3 su pagina 3" verrà aggiunto alla stessa voce INDEX di sopra.
# La parte del numero di pagina di quella voce INDEX visualizzerà ora "MySequence a 1 su pagina 2, 3 su pagina 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Inserisci un campo XE con un nuovo e unico valore della proprietà Text.
# Questo aggiungerà una nuova voce, con MySequence a 3 su pagina 4.
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

