---
title: "Método Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders. Especifica si las palabras clave para \\\"old readers\\\" se escriben en RTF o no. Esto puede afectar significativamente el tamaño del documento RTF. El valor predeterminado es true en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Especifica si las palabras clave para "old readers" se escriben en RTF o no. Esto puede afectar significativamente el tamaño del documento RTF. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Observaciones


\"Old readers\" son aplicaciones anteriores a Microsoft Word 97 y también WordPad. Cuando esta opción es **true** Aspose.Words escribe palabras clave RTF adicionales. Estas palabras clave permiten que el documento se muestre correctamente al abrirse en una aplicación \"old reader\", pero pueden aumentar significativamente el tamaño del documento.

Si estableces esta opción a **false**, entonces solo se mostrarán imágenes en formatos WMF, EMF y BMP en \"old readers\".

## Ejemplos



Muestra cómo guardar un documento en .rtf con opciones personalizadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Cree un objeto "RtfSaveOptions" para pasarlo al método "Save" del documento y modificar cómo lo guardamos en un RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Establezca la propiedad "ExportCompactSize" a "true" para
// reducir el tamaño del documento guardado a costa de la compatibilidad con texto de derecha a izquierda.
options->set_ExportCompactSize(true);

// Establezca la propiedad "ExportImagesFotOldReaders" a "true" para usar palabras clave adicionales y asegurar que nuestro documento esté
// compatible con lectores de Microsoft Word 97 anteriores y WordPad.
// Establezca la propiedad "ExportImagesFotOldReaders" a "false" para reducir el tamaño del documento,
// pero evitar que los lectores antiguos puedan leer cualquier imagen que no sea metafile o BMP que el documento pueda contener.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Ver también

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
