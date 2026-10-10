---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria"
linktitle: "get_DocumentSplitCriteria"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria. Especifica cómo se debe dividir el documento al guardarlo en formato Html, Epub o Azw3. El valor predeterminado es None para HTML y HeadingParagraph para EPUB y AZW3 en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Especifica cómo se debe dividir el documento al guardarlo en formato [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) o [Azw3](../../../aspose.words/saveformat/). El valor predeterminado es [None](../../documentsplitcriteria/) para HTML y [HeadingParagraph](../../documentsplitcriteria/) para EPUB y AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Observaciones


Normalmente querrías que un documento se guardara en HTML como un solo archivo. Pero en algunos casos es preferible dividir la salida en varias páginas HTML más pequeñas. Al guardar en formato HTML, estas páginas se exportarán a archivos o flujos individuales. Al guardar en formato EPUB se incorporarán en los paquetes correspondientes.

Un documento no puede dividirse al guardarse en formato MHTML.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
