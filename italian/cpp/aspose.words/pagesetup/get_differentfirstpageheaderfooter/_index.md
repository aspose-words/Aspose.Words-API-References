---
title: "Metodo Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter. True se un'intestazione o un piè di pagina diverso è usato nella prima pagina in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Vero se un'intestazione o un piè di pagina diverso è usato nella prima pagina.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Esempi



Mostra come abilitare o disabilitare le intestazioni/piè di pagina primari.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due tipi di intestazioni/piè di pagina.
// 1 -  L'intestazione/piè di pagina \"First\", che appare nella prima pagina della sezione.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  L'intestazione/piè di pagina \"Primary\", che appare in ogni pagina della sezione.
// Possiamo sovrascrivere l'intestazione/piè di pagina primario con un'intestazione/piè di pagina della prima e della pagina pari.
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

// Ogni sezione ha un oggetto "PageSetup" che specifica le proprietà relative all'aspetto della pagina
// come orientamento, dimensione e bordi.
// Imposta la proprietà \"DifferentFirstPageHeaderFooter\" su \"true\" per applicare l'intestazione/piè di pagina iniziale alla prima pagina.
// Imposta la proprietà \"DifferentFirstPageHeaderFooter\" su \"false\"
// per fare in modo che la prima pagina mostri l'intestazione/piè di pagina primario.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
