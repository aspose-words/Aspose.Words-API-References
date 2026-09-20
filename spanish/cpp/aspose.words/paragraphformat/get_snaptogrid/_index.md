---
title: "Método Aspose::Words::ParagraphFormat::get_SnapToGrid"
linktitle: "get_SnapToGrid"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ParagraphFormat::get_SnapToGrid. Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Especifica si el párrafo actual debe usar la configuración de líneas de cuadrícula del documento por página al organizar el contenido en el párrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
