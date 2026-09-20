---
title: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements método"
linktitle: "get_RasterizeTransformedElements"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements método. Obtiene o establece un valor que determina si los elementos transformados complejos deben rasterizarse antes de guardar en un documento PCL. El valor predeterminado es true en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/pclsaveoptions/get_rasterizetransformedelements/
---
## PclSaveOptions::get_RasterizeTransformedElements method


Obtiene o establece un valor que determina si los elementos transformados complejos deben rasterizarse antes de guardar el documento PCL. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::PclSaveOptions::get_RasterizeTransformedElements() const
```


## Ejemplos



Muestra cómo rasterizar elementos complejos al guardar un documento en PCL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Pcl);
saveOptions->set_RasterizeTransformedElements(true);

doc->Save(get_ArtifactsDir() + u"PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

## Ver también

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
