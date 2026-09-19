---
title: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator metodo"
linktitle: "get_SequenceSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldToc::get_SequenceSeparator metodo. Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.fields/fieldtoc/get_sequenceseparator/
---
## FieldToc::get_SequenceSeparator method


Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_SequenceSeparator()
```


## Esempi



Mostra come popolare un campo TOC con voci usando i campi SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che include il campo SEQ e il numero di pagina in cui il campo appare.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// I campi SEQ mostrano un conteggio che incrementa ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza nominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Usa la proprietà "TableOfFiguresLabel" per denominare una sequenza principale per il TOC.
// Ora, questo TOC creerà solo voci da campi SEQ il cui "SequenceIdentifier" è impostato su "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Possiamo denominare un'altra sequenza di campo SEQ nella proprietà "PrefixedSequenceIdentifier".
// I campi SEQ di questa sequenza prefisso non creeranno voci nel TOC.
// Ogni voce del TOC creata da un campo SEQ di sequenza principale ora visualizzerà anche il conteggio che
// la sequenza prefisso è attualmente al valore del campo SEQ di sequenza primaria che ha generato la voce.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Ogni voce del TOC visualizzerà il conteggio della sequenza prefisso immediatamente a sinistra
// del numero di pagina su cui appare il campo SEQ della sequenza principale.
// Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Esistono due modi per utilizzare i campi SEQ per popolare questo TOC.
// 1 -  Inserimento di un campo SEQ che appartiene alla sequenza prefisso del TOC:
// Questo campo incrementerà il conteggio della sequenza SEQ per "PrefixSequence" di 1.
// Poiché questo campo non appartiene alla sequenza principale identificata
// dalla proprietà "TableOfFiguresLabel" del TOC, non apparirà come voce.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Inserimento di un campo SEQ che appartiene alla sequenza principale del TOC:
// Questo campo SEQ creerà una voce nel TOC.
// La voce del TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero della pagina su cui appare.
// Questa voce visualizzerà anche il conteggio attuale della sequenza prefisso,
// separato dal numero di pagina dal valore nella proprietà SeqenceSeparator del TOC.
// Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale è a pagina 2,
// e il separatore è ">", quindi la voce visualizzerà "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Inserisci una pagina, avanza la sequenza prefisso di 2 e inserisci un campo SEQ per creare una voce del TOC successivamente.
// La sequenza prefisso è ora a 2, e il campo SEQ della sequenza principale è a pagina 3,
// quindi la voce del TOC visualizzerà "2>3" nel suo conteggio di pagina.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Vedi anche

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
