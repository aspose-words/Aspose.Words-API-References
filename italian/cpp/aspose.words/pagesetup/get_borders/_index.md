---
title: "Aspose::Words::PageSetup::get_Borders metodo"
linktitle: "get_Borders"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_Borders metodo. Ottiene una collezione dei bordi della pagina in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


Ottiene una raccolta dei bordi della pagina.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


## Esempi



Mostra come creare un bordo di pagina verde ondulato con un'ombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## Vedi anche

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
