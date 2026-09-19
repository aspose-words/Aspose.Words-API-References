---
title: "Aspose::Words::PageSetup::get_BorderSurroundsHeader metodo"
linktitle: "get_BorderSurroundsHeader"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_BorderSurroundsHeader metodo. Specifica se il bordo della pagina include o esclude l'intestazione in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/pagesetup/get_bordersurroundsheader/
---
## PageSetup::get_BorderSurroundsHeader method


Specifica se il bordo della pagina include o esclude l'intestazione.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsHeader()
```


## Esempi



Mostra come applicare un bordo alla pagina e all'intestazione/piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Inserisci un bordo blu a doppia linea.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// L'oggetto PageSetup di una sezione ha i flag "BorderSurroundsHeader" e "BorderSurroundsFooter" che determinano
// se un bordo della pagina circonda il testo principale del corpo, includendo anche l'intestazione o il piè di pagina, rispettivamente.
// Imposta il flag "BorderSurroundsHeader" su "true" per circondare l'intestazione con il nostro bordo,
// e poi imposta il flag "BorderSurroundsFooter" per lasciare il piè di pagina fuori dal bordo.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
