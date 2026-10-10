---
title: "Aspose::Words::Saving::TxtListIndentation::get_Count metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtListIndentation::get_Count metod. Hämtar eller anger hur många Character som ska användas som indrag per en listnivå. Standardvärdet är 0, vilket betyder inget indrag i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Hämtar eller anger hur många [Character](../get_character/) som ska användas som indrag per en listnivå. Standardvärdet är 0, vilket betyder inget indrag.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


## Exempel



Visar hur man konfigurerar listindentering när ett dokument sparas som klartext.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en lista med tre nivåer av indentering.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Skapa ett \"TxtSaveOptions\"-objekt, som vi kan skicka till dokumentets \"Save\"-metod
// för att ändra hur vi sparar dokumentet som ren text.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Ställ in egenskapen "Character" för att tilldela ett tecken att använda
// för utfyllnad som simulerar listindentering i klartext.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Ställ in egenskapen "Count" för att ange antalet gånger
// för att placera utfyllnadstecknet för varje listindenteringsnivå.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Se även

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
