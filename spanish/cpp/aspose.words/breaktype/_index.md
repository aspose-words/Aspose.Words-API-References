---
title: "Enumeración Aspose::Words::BreakType"
linktitle: "BreakType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::BreakType. Especifica el tipo de un salto dentro de un documento en C++."
type: docs
weight: 82000
url: /es/cpp/aspose.words/breaktype/
---
## BreakType enum


Especifica el tipo de salto dentro de un documento.

```cpp
enum class BreakType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ParagraphBreak | 0 | Salto entre párrafos. |
| PageBreak | 1 | Salto de página explícito. |
| ColumnBreak | 2 | Salto de columna explícito. |
| SectionBreakContinuous | 3 | Especifica el inicio de una nueva sección en la misma página que la sección anterior. |
| SectionBreakNewColumn | 4 | Especifica el inicio de una nueva sección en la nueva columna. |
| SectionBreakNewPage | 5 | Especifica el inicio de una nueva sección en una nueva página. |
| SectionBreakEvenPage | 6 | Especifica el inicio de una nueva sección en una página par nueva. |
| SectionBreakOddPage | 7 | Especifica el inicio de una nueva sección en una página impar. |
| LineBreak | 8 | Salto de línea explícito. |


## Ejemplos



Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una tabla de contenido para la primera página del documento.
// Configura la tabla para que incluya párrafos con encabezados de niveles 1 a 3.
// Además, configura sus entradas para que sean hipervínculos que nos llevarán
// a la ubicación del encabezado al hacer clic izquierdo en Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Poblar el índice añadiendo párrafos con estilos de encabezado.
// Cada encabezado de este tipo con un nivel entre 1 y 3 creará una entrada en el índice.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Un índice es un campo de un tipo que necesita actualizarse para mostrar un resultado actualizado.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Muestra cómo aplicar y revertir la configuración de página en secciones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifique las propiedades de configuración de página de la sección actual del generador y añada texto.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Si iniciamos una nueva sección usando un generador de documentos,
// heredará las propiedades de configuración de página actuales del generador.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Podemos revertir sus propiedades de configuración de página a sus valores predeterminados usando el método "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
