---
title: "Aspose::Words::Document::get_LastSection method"
linktitle: "get_LastSection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_LastSection method. Hämtar den sista sektionen i dokumentet i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Hämtar den sista sektionen i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Exempel



Visar hur man skapar en ny sektion med en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett tomt dokument innehåller en sektion som standard,
// som innehåller underordnade noder som vi kan redigera.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Använd en dokumentbyggare för att lägga till text i den första sektionen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Skapa en andra sektion genom att infoga ett sektionsavbrott.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Varje sektion har sina egna sidinställningar.
// Vi kan dela upp texten i den andra sektionen i två kolumner.
// Detta kommer inte att påverka texten i den första sektionen.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## Se även

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
