---
title: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto method"
linktitle: "get_SpaceBeforeAuto"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto method. Sant om mängden avstånd före stycket sätts automatiskt i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/paragraphformat/get_spacebeforeauto/
---
## ParagraphFormat::get_SpaceBeforeAuto method


Sant om mängden avstånd före stycket sätts automatiskt.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto()
```

## Anmärkningar


När den är inställd på **true**, åsidosätter effekten av [SpaceBefore](../get_spacebefore/).

När du ställer in styckets Space Before och Space After till Auto, lägger **Microsoft** Word automatiskt till 14 punkters avstånd mellan stycken enligt följande regler:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



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

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
