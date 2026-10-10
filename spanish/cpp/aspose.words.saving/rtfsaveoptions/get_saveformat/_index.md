---
title: "Método Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser Rtf en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/rtfsaveoptions/get_saveformat/
---
## RtfSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Rtf](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
