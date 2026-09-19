---
title: "Metodo Aspose::Words::Fields::FieldSeq::get_ResetNumber"
linktitle: "get_ResetNumber"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldSeq::get_ResetNumber. Ottiene o imposta un numero intero a cui ripristinare il numero di sequenza. Restituisce -1 se il numero è assente in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/fieldseq/get_resetnumber/
---
## FieldSeq::get_ResetNumber method


Ottiene o imposta un numero intero a cui ripristinare il numero di sequenza. Restituisce -1 se il numero è assente.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_ResetNumber()
```


## Esempi



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
