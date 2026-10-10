---
title: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator metodo"
linktitle: "get_SequenceSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldIndex::get_SequenceSeparator metodo. Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.fields/fieldindex/get_sequenceseparator/
---
## FieldIndex::get_SequenceSeparator method


Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_SequenceSeparator()
```


## Esempi



Mostra come suddividere un documento in parti combinando i campi INDEX e SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Creare un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce mostrerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sul lato destro.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Text",
// il campo INDEX li raggrupperà in un'unica voce.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Nella proprietà SequenceName, denomina una sequenza di campo SEQ. Ogni voce di questo campo INDEX ora visualizzerà anche
// il numero corrispondente al conteggio della sequenza nella posizione del campo XE che ha creato questa voce.
index->set_SequenceName(u"MySequence");

// Imposta il testo che circonderà la sequenza e i numeri di pagina per spiegare il loro significato all'utente.
// Una voce creata con questa configurazione visualizzerà qualcosa come "MySequence at 1 on page 1" al suo numero di pagina.
// PageNumberSeparator e SequenceSeparator non possono superare i 15 caratteri.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// I campi SEQ mostrano un conteggio che incrementa ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza nominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che sposta la sequenza "MySequence" a 1.
// Questo campo non è diverso dal testo normale del documento. Non apparirà nell'indice di un campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Inserisci un campo XE che creerà una voce nel campo INDEX.
// Poiché "MySequence" è a 1 e questo campo XE è a pagina 2, insieme ai separatori personalizzati che abbiamo definito sopra,
// la voce INDEX di questo campo visualizzerà "Cat" sul lato sinistro e "MySequence at 1 on page 2" sul lato destro.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Inserisci un'interruzione di pagina e usa i campi SEQ per avanzare "MySequence" a 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Inserisci un campo XE con la stessa proprietà Text del precedente.
// La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Text".
// in un'unica voce invece di creare una voce per ogni campo XE.
// Poiché siamo a pagina 2 con "MySequence" a 3, ", 3 on page 3" verrà aggiunto alla stessa voce INDEX di sopra.
// La parte del numero di pagina di quella voce INDEX visualizzerà ora "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Inserisci un campo XE con un nuovo valore unico per la proprietà Text.
// Questo aggiungerà una nuova voce, con MySequence a 3 a pagina 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Vedi anche

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
