---
title: "Aspose::Words::SectionLayoutMode enumeración"
linktitle: "SectionLayoutMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SectionLayoutMode enumeración. Especifica el modo de diseño para una sección que permite definir el comportamiento de la cuadrícula del documento en C++."
type: docs
weight: 115000
url: /es/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Especifica el modo de diseño para una sección que permite definir el comportamiento de la cuadrícula del documento.

```cpp
enum class SectionLayoutMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Predeterminado | 0 | Especifica que no se aplicará ninguna cuadrícula de documento al contenido de la sección correspondiente en el documento. |
| Cuadrícula | 1 | Especifica que la sección correspondiente tendrá tanto el interlineado adicional como el espaciado de caracteres añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres no se alinearán automáticamente con las líneas de la cuadrícula al escribir. |
| LineGrid | 2 | Especifica que la sección correspondiente tendrá un interlineado adicional añadido a cada línea dentro de ella para mantener el número especificado de líneas por página. |
| SnapToChars | 3 | Especifica que la sección correspondiente tendrá tanto el interlineado adicional como el espaciado de caracteres añadido a cada línea y carácter dentro de ella para mantener un número específico de líneas por página y caracteres por línea. Los caracteres se alinearán automáticamente con las líneas de la cuadrícula al escribir. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
