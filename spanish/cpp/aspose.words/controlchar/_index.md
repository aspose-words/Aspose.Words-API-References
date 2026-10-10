---
title: "Aspose::Words::ControlChar clase"
linktitle: "ControlChar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ControlChar clase. Los caracteres de control se encuentran a menudo en documentos. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words/controlchar/
---
## ControlChar class


Caracteres de control que se encuentran a menudo en documentos. Para obtener más información, visite el artículo de documentación [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Cell](./cell/)() | Carácter de fin de una celda de tabla o fin de una fila de tabla: "\x0007" o "\a". |
| static [ColumnBreak](./columnbreak/)() | Carácter de fin de columna: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Carácter de retorno de carro: "\x000d" o "\r". Igual que [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Retorno de carro seguido de carácter de salto de línea: "\x000d\x000a" o "\r\n". No se usa así en documentos de Microsoft Word, pero se usa comúnmente en archivos de texto para saltos de párrafo. |
| static [Lf](./lf/)() | Carácter de salto de línea: "\x000a" o "\n". Igual que [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Carácter de salto de línea: "\x000b" o "\v". |
| static [LineFeed](./linefeed/)() | Carácter de salto de línea: "\x000a" o "\n". Igual que [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Carácter de espacio de no separación: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Carácter de salto de página: "\x000c" o "\f". Nota que tiene el mismo valor que [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Carácter de fin de párrafo: "\x000d" o "\r". Igual que [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Carácter de fin de sección: "\x000c" o "\f". Nota que tiene el mismo valor que [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Carácter de tabulación: "\x0009" o "\t". |
## Campos

| Campo | Descripción |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Carácter de fin de una celda de tabla o fin de una fila de tabla: (char)7 o "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Carácter de fin de columna: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Este es el carácter "o" usado como valor predeterminado en los campos de formulario de entrada de texto. |
| static constexpr [FieldEndChar](./fieldendchar/) | Carácter de fin de campo MS Word: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | El carácter separador de campo separa el código del campo del valor del campo. Opcional en algunos campos. Valor: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Carácter de inicio de campo MS Word: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Carácter de salto de línea: (char)11 o "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Carácter de salto de línea: (char)10 o "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | El guion no separable en Microsoft Word es (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Carácter de espacio no separable: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | El guion opcional en Microsoft Word es (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Carácter de salto de página: (char)12 o "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Carácter de fin de párrafo: (char)13 o "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Carácter de fin de sección: (char)12 o "\f". |
| static constexpr [SpaceChar](./spacechar/) | Carácter de espacio: (char)32. |
| static constexpr [TabChar](./tabchar/) | Carácter de tabulación: (char)9 o "\t". |

## Ejemplos



Muestra cómo usar caracteres de control.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta párrafos con texto usando DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Convertir el documento a formato de texto revela que los caracteres de control
// representan algunos de los elementos estructurales del documento, como saltos de página.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Al convertir un documento a forma de cadena,
// podemos omitir algunos de los caracteres de control con el método Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
