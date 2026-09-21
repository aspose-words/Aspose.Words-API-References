---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent method"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent method. Hämtar eller anger värdet (i punkter) som representerar vänsterindraget för stycket i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


Hämtar eller anger värdet (i punkter) som representerar vänsterindrag för stycket.

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## Exempel



Visar hur man konfigurerar styckeformatering för att skapa text som inte är centrerad.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Centrera all text som dokumentbyggaren skriver, och ställ in indrag.
// Indentkonfigurationen nedan kommer att skapa en textblock som sitter asymmetriskt på sidan.
// Det \"center\" som vi justerar texten mot kommer att vara mitten av textblocket, inte mitten av sidan.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
