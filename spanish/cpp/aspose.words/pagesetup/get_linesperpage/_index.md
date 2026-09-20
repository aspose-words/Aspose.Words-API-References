---
title: "Aspose::Words::PageSetup::get_LinesPerPage método"
linktitle: "get_LinesPerPage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_LinesPerPage método. Obtiene o establece el número de líneas por página en la cuadrícula del documento en C++."
type: docs
weight: 26000
url: /es/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Obtiene o establece el número de líneas por página en la cuadrícula del documento.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Observaciones


El valor mínimo de la propiedad es 1. El valor máximo depende de la altura de la página y del tamaño de fuente del estilo Normal. El paso mínimo de línea es el 136 por ciento del tamaño de fuente. Por ejemplo, el número máximo de líneas por página de una página Letter con márgenes de una pulgada es 39.

Por defecto, la propiedad tiene un valor en el que el paso de línea es 1,5 veces mayor que el tamaño de fuente del estilo Normal.

## Ejemplos



Muestra cómo especificar un límite para el número de líneas que puede tener cada página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Habilite el ajuste de interlineado y luego úselo para establecer el número de líneas por página en esta sección.
// Un tamaño de fuente lo suficientemente grande empujará algunas líneas a la página siguiente para evitar la superposición de caracteres.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
