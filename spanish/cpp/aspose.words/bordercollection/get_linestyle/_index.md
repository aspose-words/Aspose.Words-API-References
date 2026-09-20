---
title: "Aspose::Words::BorderCollection::get_LineStyle método"
linktitle: "get_LineStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::BorderCollection::get_LineStyle método. Obtiene o establece el estilo del borde en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Obtiene o establece el estilo del borde.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Observaciones


Devuelve el estilo del primer borde de la colección.

Establece el estilo de todos los bordes de la colección excluyendo los bordes diagonales.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
