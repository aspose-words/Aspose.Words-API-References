---
title: "Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier metodo"
linktitle: "get_SequenceIdentifier"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier metodo. Ottiene o imposta il nome assegnato alla serie di elementi da numerare in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fields/fieldseq/get_sequenceidentifier/
---
## FieldSeq::get_SequenceIdentifier method


Ottiene o imposta il nome assegnato alla serie di elementi da numerare.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier()
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


Mostra la creazione della numerazione usando i campi SEQ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// I campi SEQ mostrano un conteggio che incrementa ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza nominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che visualizzi il valore corrente del conteggio di "MySequence",
// dopo aver usato la proprietà "ResetNumber" per impostarlo a 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Visualizza il numero successivo in questa sequenza con un altro campo SEQ.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Inserisci un'intestazione di livello 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Inserisci un altro campo SEQ dalla stessa sequenza e configurarlo per azzerare il conteggio a ogni intestazione con 1.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// L'intestazione sopra è di livello 1, quindi il conteggio per questa sequenza viene azzerato a 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Passa al numero successivo di questa sequenza.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```

## Vedi anche

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
