---
title: "Aspose::Words::BreakType enum"
linktitle: "BreakType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BreakType enum. Anger typen av ett avbrott i ett dokument i C++."
type: docs
weight: 82000
url: /sv/cpp/aspose.words/breaktype/
---
## BreakType enum


Anger typen av ett avbrott i ett dokument.

```cpp
enum class BreakType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| ParagraphBreak | 0 | Avbrott mellan stycken. |
| PageBreak | 1 | Explicit sidbrytning. |
| ColumnBreak | 2 | Explicit kolumnbrytning. |
| SectionBreakContinuous | 3 | Anger start av ny sektion på samma sida som föregående sektion. |
| SectionBreakNewColumn | 4 | Anger start av ny sektion i den nya kolumnen. |
| SectionBreakNewPage | 5 | Anger start av ny sektion på en ny sida. |
| SectionBreakEvenPage | 6 | Anger start av ny sektion på en ny jämn sida. |
| SectionBreakOddPage | 7 | Anger start av ny sektion på en udda sida. |
| LineBreak | 8 | Explicit radbrytning. |


## Exempel



Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med rubrikstilar som poster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen så att den plockar upp stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster så att de blir hyperlänkar som tar oss
// till rubrikens plats när de vänsterklickas i Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Fyll i innehållsförteckningen genom att lägga till stycken med rubrikstilar.
// Varje sådan rubrik med en nivå mellan 1 och 3 kommer att skapa en post i tabellen.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// En innehållsförteckning är ett fält av en typ som måste uppdateras för att visa ett aktuellt resultat.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Visar hur man tillämpar och återställer sidinställningar för sektioner i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ändra sidinställningarnas egenskaper för byggarens aktuella sektion och lägg till text.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Om vi startar en ny sektion med en dokumentbyggare,
// kommer den att ärva byggarens aktuella sidinställningsegenskaper.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Vi kan återställa dess sidinställningsegenskaper till deras standardvärden med metoden "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
