---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding método"
linktitle: "get_Encoding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding método. Especifica la codificación a usar al exportar a HTML, MHTML o EPUB. El valor predeterminado es new UTF8Encoding(false) (UTF-8 sin BOM) en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_encoding/
---
## HtmlSaveOptions::get_Encoding method


Especifica la codificación a usar al exportar a HTML, MHTML o EPUB. El valor predeterminado es **new UTF8Encoding(false)** (UTF-8 sin BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlSaveOptions::get_Encoding() const
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
