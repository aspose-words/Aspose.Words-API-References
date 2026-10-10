---
title: "Aspose::Words::Fields::FieldSubject::get_Text metodo"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSubject::get_Text metodo. Ottiene o imposta il testo del soggetto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Ottiene o imposta il testo del soggetto.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Esempi



Mostra come utilizzare il campo SUBJECT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Imposta un valore per la proprietà incorporata "Subject" del documento.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Crea un campo SUBJECT per visualizzare il valore di quella proprietà incorporata.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Se forniamo il valore della proprietà Text del campo SUBJECT e lo aggiorniamo, il campo lo farà
// sovrascrive il valore corrente della proprietà incorporata \"Subject\" con il valore della sua proprietà Text,
// e poi visualizzerà il nuovo valore.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Vedi anche

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
