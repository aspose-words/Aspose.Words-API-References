---
title: "Método Aspose::Words::PageSetup::get_Borders"
linktitle: "get_Borders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_Borders. Obtiene una colección de los bordes de página en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


Obtiene una colección de los bordes de página.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


## Ejemplos



Muestra cómo crear un borde de página ondulado verde con una sombra.
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

## Ver también

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
