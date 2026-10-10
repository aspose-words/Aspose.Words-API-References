---
title: "Aspose::Words::BorderCollection::get_Color método"
linktitle: "get_Color"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BorderCollection::get_Color método. Obtiene o establece el color del borde en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Obtiene o establece el color del borde.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Observaciones


Devuelve el color del primer borde de la colección.

Establece el color de todos los bordes de la colección, excluyendo los bordes diagonales.

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
