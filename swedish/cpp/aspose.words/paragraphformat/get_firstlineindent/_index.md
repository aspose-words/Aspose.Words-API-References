---
title: "Aspose::Words::ParagraphFormat::get_FirstLineIndent‑metod"
linktitle: "get_FirstLineIndent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_FirstLineIndent‑metod. Hämtar eller anger värdet (i punkter) för ett första radindrag eller hängande indrag. Använd positiva värden för att ange första radindraget och negativa värden för att ange hängande indrag i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Hämtar eller anger värdet (i punkter) för första raden eller hängande indrag. Använd positiva värden för att ange första radens indrag och negativa värden för att ange hängande indrag.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
```


## Exempel



Visar hur man infogar ett stycke i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// Metoden "Writeln" avslutar stycket efter att ha lagt till text
// och startar sedan en ny rad, vilket lägger till ett nytt stycke.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
