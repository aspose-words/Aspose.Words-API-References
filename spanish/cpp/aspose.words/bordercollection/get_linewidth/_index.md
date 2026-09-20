---
title: "Aspose::Words::BorderCollection::get_LineWidth método"
linktitle: "get_LineWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BorderCollection::get_LineWidth método. Obtiene o establece el ancho del borde en puntos en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


Obtiene o establece el ancho del borde en puntos.

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## Observaciones


Devuelve el ancho del primer borde de la colección.

Establece el ancho de todos los bordes de la colección, excluyendo los bordes diagonales.

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

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
