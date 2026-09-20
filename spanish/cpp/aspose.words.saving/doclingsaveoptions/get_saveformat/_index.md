---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat método"
linktitle: "get_SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat método. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser Docling en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/doclingsaveoptions/get_saveformat/
---
## DoclingSaveOptions::get_SaveFormat method


Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Sólo puede ser [Docling](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::DoclingSaveOptions::get_SaveFormat() override
```


## Ejemplos



Muestra cómo guardar un documento en formato JSON Docling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Establezca en true para renderizar las formas que no son imágenes e incluirlas en la salida.
// Establezca en false (por defecto) para excluir las formas que no son imágenes de la salida.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
