---
title: "Aspose::Words::PageSetup::get_BorderSurroundsHeader-metod"
linktitle: "get_BorderSurroundsHeader"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_BorderSurroundsHeader-metod. Anger om sidans kant inkluderar eller exkluderar rubriken i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/pagesetup/get_bordersurroundsheader/
---
## PageSetup::get_BorderSurroundsHeader method


Anger om sidramen inkluderar eller exkluderar sidhuvudet.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsHeader()
```


## Exempel



Visar hur man applicerar en ram på sidan samt sidhuvud/sidfötter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Infoga en blå dubbelradig ram.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Ett avsnitts PageSetup‑objekt har flaggorna "BorderSurroundsHeader" och "BorderSurroundsFooter" som bestämmer
// om en sidram omger huvudtexten, samt om den inkluderar sidhuvudet eller sidfoten respektive.
// Ställ in flaggan "BorderSurroundsHeader" till "true" för att omge sidhuvudet med vår ram,
// och sedan sätt flaggan "BorderSurroundsFooter" för att låta sidfoten ligga utanför kanten.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
