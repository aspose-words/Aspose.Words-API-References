---
title: "Metodo Aspose::Words::PageSetup::get_RestartPageNumbering"
linktitle: "get_RestartPageNumbering"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_RestartPageNumbering. True se la numerazione delle pagine ricomincia all'inizio della sezione in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words/pagesetup/get_restartpagenumbering/
---
## PageSetup::get_RestartPageNumbering method


Vero se la numerazione delle pagine ricomincia all'inizio della sezione.

```cpp
bool Aspose::Words::PageSetup::get_RestartPageNumbering()
```


## Esempi



Mostra come impostare la numerazione delle pagine in una sezione.
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

// Sposta il document builder nell'intestazione primaria della prima sezione,
// che verrà visualizzata su ogni pagina di quella sezione.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Inserisci un campo PAGE, che visualizzerà il numero della pagina corrente.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configura la sezione in modo che il conteggio delle pagine visualizzato dai campi PAGE inizi da 5.
// Inoltre, configura tutti i campi PAGE per visualizzare i loro numeri di pagina usando numeri romani maiuscoli.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Crea un'altra intestazione primaria per la seconda sezione, con un altro campo PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configura la sezione in modo che il conteggio delle pagine visualizzato dai campi PAGE inizi da 10.
// Inoltre, configura tutti i campi PAGE per visualizzare i loro numeri di pagina usando numeri arabi.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
