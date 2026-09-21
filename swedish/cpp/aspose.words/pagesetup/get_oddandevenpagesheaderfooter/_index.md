---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter metod"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter metod. Sant om dokumentet har olika sidhuvuden och sidfötter för udda och jämna sidor i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Sant om dokumentet har olika sidhuvuden och sidfötter för udda och jämna sidor.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Exempel



Visar hur man aktiverar eller inaktiverar sidhuvuden/sidfötter för jämna sidor.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan finns två typer av sidhuvuden/sidfötter.
// 1 -  Det "Primära" sidhuvudet/sidfoten, som visas på varje sida i avsnittet.
// Vi kan åsidosätta det primära sidhuvudet/sidfoten med ett första och ett jämnt sidhuvud/sidfötter.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  Det "Jämna" sidhuvudet/sidfoten, som visas på varje jämn sida i detta avsnitt.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Varje avsnitt har ett "PageSetup"-objekt som specificerar egenskaper relaterade till sidans utseende
// såsom orientering, storlek och kanter.
// Ställ in egenskapen "OddAndEvenPagesHeaderFooter" till "true"
// för att visa sidhuvudet/sidfoten för jämna sidor på jämna sidor.
// Ställ in egenskapen "OddAndEvenPagesHeaderFooter" till "false"
// för att visa det primära sidhuvudet/sidfoten på jämna sidor.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
