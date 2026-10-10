---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfter method"
linktitle: "get_SpaceAfter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfter method. Hämtar eller anger mängden mellanrum (i punkter) efter stycket i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words/paragraphformat/get_spaceafter/
---
## ParagraphFormat::get_SpaceAfter method


Hämtar eller anger mängden avstånd (i punkter) efter stycket.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceAfter()
```

## Anmärkningar


Har ingen effekt när [SpaceAfterAuto](../get_spaceafterauto/) är **true**.

Giltiga värden sträcker sig från 0 till 1584 inklusive.

## Exempel



Visar hur man ställer in automatisk styckeavstånd.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tillämpa en stor mängd avstånd före och efter stycken som denna byggare kommer att skapa.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Ställ in dessa flaggor till "true" för att tillämpa automatisk mellanrum,
// och effektivt ignorerar mellanrummet i de egenskaper vi angav ovan.
// Att lämna dem som "false" kommer att tillämpa vårt anpassade styckeavstånd.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Infoga två stycken som kommer att ha mellanrum ovanför och nedanför dem och spara dokumentet.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


Visar hur man tillämpar ingen avstånd mellan stycken med samma stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tillämpa en stor mängd avstånd före och efter stycken som denna byggare kommer att skapa.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Ställ in flaggan "NoSpaceBetweenParagraphsOfSameStyle" till "true" för att tillämpa
// ingen mellanrum mellan stycken med samma stil, vilket kommer att gruppera liknande stycken.
// Lämna flaggan "NoSpaceBetweenParagraphsOfSameStyle" som "false"
// för att jämnt tillämpa mellanrum på varje stycke.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
