---
title: "Aspose::Words::DocumentBuilder::InsertParagraph metod"
linktitle: "InsertParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::InsertParagraph metod. Infogar ett styckeavbrott i dokumentet i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Infogar en styckebrytning i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Styckets nod som just infogades. Det är samma nod som [CurrentParagraph](../get_currentparagraph/).
## Anmärkningar


Formateringen för aktuellt stycke som anges av egenskapen [ParagraphFormat](../get_paragraphformat/) används.

Delar det aktuella stycket i två. Efter att stycket har infogats placeras markören i början av det nya stycket.

Ett undantag kastas om det inte är möjligt att infoga ett styckeavbrott vid den aktuella markörpositionen.

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

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
