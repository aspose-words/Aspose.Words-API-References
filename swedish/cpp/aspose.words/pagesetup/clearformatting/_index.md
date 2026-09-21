---
title: "Aspose::Words::PageSetup::ClearFormatting-metod"
linktitle: "ClearFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::ClearFormatting-metod. Återställer sidinställningarna till standardpappersstorlek, marginaler och orientering i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/pagesetup/clearformatting/
---
## PageSetup::ClearFormatting method


Återställer sidinställningarna till standardpappersstorlek, marginaler och orientering.

```cpp
void Aspose::Words::PageSetup::ClearFormatting()
```


## Exempel



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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
