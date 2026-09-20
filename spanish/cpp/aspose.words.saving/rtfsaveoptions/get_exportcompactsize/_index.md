---
title: "Método Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize"
linktitle: "get_ExportCompactSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize. Permite que los documentos RTF de salida sean más pequeños, pero si contienen texto RTL (de derecha a izquierda), no se mostrará correctamente. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Permite que los documentos RTF de salida sean más pequeños en tamaño, pero si contienen texto RTL (de derecha a izquierda), no se mostrará correctamente. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Observaciones


Si el documento que desea convertir a RTF usando Aspose.Words no contiene texto de derecha a izquierda en idiomas como el árabe, entonces puede establecer esta opción a **true** para reducir el tamaño del RTF resultante.

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
