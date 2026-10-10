---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties"
linktitle: "get_ExportDocumentProperties"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties. Especifica si se deben exportar las propiedades del documento incorporadas y personalizadas a HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportdocumentproperties/
---
## HtmlSaveOptions::get_ExportDocumentProperties method


Especifica si se deben exportar las propiedades de documento incorporadas y personalizadas a HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties() const
```


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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
