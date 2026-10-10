---
title: "Aspose::Words::BorderCollection::get_DistanceFromText método"
linktitle: "get_DistanceFromText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BorderCollection::get_DistanceFromText método. Obtiene o establece la distancia del borde al texto en puntos en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Obtiene o establece la distancia del borde al texto en puntos.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Observaciones


Obtiene la distancia del texto para el primer borde.

Establece la distancia del texto para todos los bordes de la colección, excluyendo los bordes diagonales.

No tiene efecto y se restablecerá automáticamente a cero para los bordes de las celdas de tabla.

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
