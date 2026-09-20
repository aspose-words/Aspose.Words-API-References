---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution"
linktitle: "get_ImageResolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution. Especifica la resolución de salida para las imágenes al exportar a Markdown. El valor predeterminado es %96 dpi en C++."
type: docs
weight: 3750
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Especifica la resolución de salida para las imágenes al exportar a Markdown. El valor predeterminado es **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Ejemplos



Muestra cómo establecer la resolución de salida para las imágenes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Ver también

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
