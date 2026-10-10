---
title: "Aspose::Words::PageSetup::get_PageNumberStyle metod"
linktitle: "get_PageNumberStyle"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_PageNumberStyle metod. Hämtar eller anger sidnumreringens format i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/pagesetup/get_pagenumberstyle/
---
## PageSetup::get_PageNumberStyle method


Hämtar eller anger sidnumreringsformatet.

```cpp
Aspose::Words::NumberStyle Aspose::Words::PageSetup::get_PageNumberStyle()
```


## Exempel



Visar hur man ställer in sidnumrering i en sektion.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Flytta dokumentbyggaren till den första sektionens primära sidhuvud,
// vilket varje sida i den sektionen kommer att visa.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Infoga ett PAGE‑fält, som kommer att visa numret på den aktuella sidan.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Konfigurera sektionen så att sidantalet som PAGE‑fält visar startar från 5.
// Konfigurera också alla PAGE‑fält att visa sina sidnummer med versala romerska siffror.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Skapa ett annat primärt sidhuvud för den andra sektionen, med ett annat PAGE‑fält.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Konfigurera sektionen så att sidantalet som PAGE‑fält visar startar från 10.
// Konfigurera också alla PAGE‑fält att visa sina sidnummer med arabiska siffror.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Se även

* Enum [NumberStyle](../../numberstyle/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
