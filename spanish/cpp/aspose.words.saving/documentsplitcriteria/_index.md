---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Especifica cómo se divide el documento en partes al guardarlo en formato Html, Epub o Azw3 en C++."
type: docs
weight: 52000
url: /es/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Especifica cómo se divide el documento en partes al guardarlo en formato [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) o [Azw3](../../aspose.words/saveformat/).

```cpp
enum class DocumentSplitCriteria
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | El documento no se divide. |
| PageBreak | 1 | El documento se divide en partes en saltos de página explícitos. Un salto de página puede especificarse mediante un carácter [PageBreak](../../aspose.words/controlchar/pagebreak/), un salto de sección que indique el inicio de una nueva sección en una nueva página, o un párrafo que tenga su propiedad [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) establecida en **true**. |
| ColumnBreak | 2 | El documento se divide en partes en saltos de columna. Un salto de columna puede especificarse mediante un carácter [ColumnBreak](../../aspose.words/controlchar/columnbreak/) o un salto de sección que indique el inicio de una nueva sección en una nueva columna. |
| SectionBreak | 4 | El documento se divide en partes en un salto de sección de cualquier tipo. |
| HeadingParagraph | 8 | El documento se divide en partes en un párrafo formateado con un estilo de encabezado **Heading 1**, **Heading 2**, etc. Úselo junto con [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) para especificar los niveles de encabezado (del 1 al nivel especificado) en los que dividir. |

## Observaciones


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Los criterios diferentes pueden superponerse parcialmente. Por ejemplo, el estilo **Heading 1** suele recibir la propiedad [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/), por lo que entra en dos criterios: [PageBreak](./) y [HeadingParagraph](./). Algunos saltos de sección pueden provocar saltos de página, etc. En casos típicos, especificar solo una bandera es la opción más práctica.

## Ejemplos



Muestra cómo usar una codificación específica al guardar un documento en .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Utilice un objeto SaveOptions para especificar la codificación de un documento que vamos a guardar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Por defecto, un documento .epub de salida tendrá todo su contenido en una sola parte HTML.
// Un criterio de división nos permite segmentar el documento en varias partes HTML.
// Estableceremos los criterios para dividir el documento en párrafos de encabezado.
// Esto es útil para los lectores que no pueden leer archivos HTML mayores que un tamaño específico.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Especifique que queremos exportar las propiedades del documento.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
