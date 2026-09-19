---
title: "Aspose::Words::Fields::FieldTitle::get_Text metodo"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldTitle::get_Text. Ottiene o imposta il testo del titolo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Ottiene o imposta il testo del titolo.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Esempi



Mostra come utilizzare il campo TITLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Imposta un valore per la proprietà documento incorporata "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Possiamo usare il campo TITLE per visualizzare il valore di questa proprietà nel documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Impostare un valore per la proprietà Text del campo,
// e quindi aggiornare il campo sovrascriverà anche la proprietà incorporata corrispondente con il nuovo valore.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## Vedi anche

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
