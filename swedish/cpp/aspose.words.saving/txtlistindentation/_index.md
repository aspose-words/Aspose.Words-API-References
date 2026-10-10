---
title: "Aspose::Words::Saving::TxtListIndentation class"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtListIndentation class. Anger hur listnivåer indenteras när dokumentet exporteras till Text-format. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 32000
url: /sv/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Anger hur listnivåer indenteras när dokumentet exporteras till [Text](../../aspose.words/saveformat/) format. För att lära dig mer, besök artikeln [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) i dokumentationen.

```cpp
class TxtListIndentation : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Character](./get_character/)() const | Hämtar eller anger vilket tecken som ska användas för att indentera listnivåer. Standardvärdet är '\\0', vilket betyder att det inte finns någon indentering. |
| [get_Count](./get_count/)() const | Hämtar eller anger hur många [Character](./get_character/) som ska användas som indentering per en listnivå. Standardvärdet är 0, vilket betyder ingen indentering. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | Inställare för [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | Inställare för [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
