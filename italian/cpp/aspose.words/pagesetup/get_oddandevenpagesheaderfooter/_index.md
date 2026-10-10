---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter metodo"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter method. Vero se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Vero se il documento ha intestazioni e piè di pagina diversi per le pagine dispari e pari.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Esempi



Mostra come abilitare o disabilitare le intestazioni/piè di pagina delle pagine pari.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di intestazioni/piè di pagina.
// 1 -  L'intestazione/piè di pagina "Primario", che appare su ogni pagina nella sezione.
// Possiamo sovrascrivere l'intestazione/piè di pagina primario con un'intestazione/piè di pagina della prima e della pagina pari.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  L'intestazione/piè di pagina "Pari", che appare su ogni pagina pari di questa sezione.
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

// Ogni sezione ha un oggetto "PageSetup" che specifica le proprietà relative all'aspetto della pagina
// come orientamento, dimensione e bordi.
// Imposta la proprietà "OddAndEvenPagesHeaderFooter" su "true"
// per visualizzare l'intestazione/piè di pagina delle pagine pari sulle pagine pari.
// Imposta la proprietà "OddAndEvenPagesHeaderFooter" su "false"
// per visualizzare l'intestazione/piè di pagina primario sulle pagine pari.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
