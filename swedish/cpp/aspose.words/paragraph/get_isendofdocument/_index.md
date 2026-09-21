---
title: "Aspose::Words::Paragraph::get_IsEndOfDocument method"
linktitle: "get_IsEndOfDocument"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Paragraph::get_IsEndOfDocument method. Sant om detta stycke är det sista stycket i det sista avsnittet av dokumentet i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


Sant om detta stycke är det sista stycket i den sista sektionen i dokumentet.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
