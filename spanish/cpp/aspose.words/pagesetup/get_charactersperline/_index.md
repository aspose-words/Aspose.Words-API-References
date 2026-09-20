---
title: "Método Aspose::Words::PageSetup::get_CharactersPerLine"
linktitle: "get_CharactersPerLine"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_CharactersPerLine. Obtiene o establece el número de caracteres por línea en la cuadrícula del documento en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Obtiene o establece el número de caracteres por línea en la cuadrícula del documento.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Observaciones


El valor mínimo de la propiedad es 1. El valor máximo depende del ancho de página y del tamaño de fuente del estilo Normal. El paso mínimo de carácter es el 90 por ciento del tamaño de fuente. Por ejemplo, el número máximo de caracteres por línea de una página Letter con márgenes de una pulgada es 43.

Por defecto, la propiedad tiene un valor en el que el paso de carácter es igual al tamaño de fuente del estilo Normal.

## Ejemplos



Muestra cómo especificar un límite para el número de caracteres que cada línea puede tener.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Habilite el ajuste de interlineado y luego úselo para establecer el número de caracteres por línea en esta sección.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// El número de caracteres también depende del tamaño de la fuente.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
