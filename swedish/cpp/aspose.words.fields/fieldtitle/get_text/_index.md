---
title: "Aspose::Words::Fields::FieldTitle::get_Text-metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldTitle::get_Text-metod. Hämtar eller anger texten för titeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Hämtar eller anger texten för titeln.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Exempel



Visar hur man använder TITLE-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ange ett värde för den inbyggda dokumentegenskapen "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Vi kan använda TITLE-fältet för att visa värdet av den här egenskapen i dokumentet.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Sätter ett värde för fältets Text-egenskap,
// och sedan kommer en uppdatering av fältet också att skriva över motsvarande inbyggda egenskap med det nya värdet.
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

## Se även

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
