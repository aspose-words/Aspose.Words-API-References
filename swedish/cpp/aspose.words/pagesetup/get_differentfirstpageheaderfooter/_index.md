---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter metod"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter metod. Sant om ett annat sidhuvud eller sidfot används på den första sidan i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Sant om ett annat sidhuvud eller sidfot används på första sidan.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Exempel



Visar hur man aktiverar eller inaktiverar primära sidhuvuden/sidfötter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan finns två typer av sidhuvuden/sidfötter.
// 1 -  Det "Första" sidhuvudet/sidfoten, som visas på den första sidan i avsnittet.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  Det "Primära" sidhuvudet/sidfoten, som visas på varje sida i avsnittet.
// Vi kan åsidosätta det primära sidhuvudet/sidfoten med ett första och ett jämnt sidhuvud/sidfötter.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Varje avsnitt har ett "PageSetup"-objekt som specificerar egenskaper relaterade till sidans utseende
// såsom orientering, storlek och kanter.
// Ställ in egenskapen "DifferentFirstPageHeaderFooter" till "true" för att tillämpa det första sidhuvudet/sidfoten på den första sidan.
// Ställ in egenskapen "DifferentFirstPageHeaderFooter" till "false"
// för att låta den första sidan visa det primära sidhuvudet/sidfoten.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
