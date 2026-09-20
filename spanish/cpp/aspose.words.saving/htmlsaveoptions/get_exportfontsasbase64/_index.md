---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 método"
linktitle: "get_ExportFontsAsBase64"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 método. Especifica si los recursos de fuentes deben incrustarse en HTML con codificación Base64. El valor predeterminado es false en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Especifica si los recursos de fuentes deben incrustarse en HTML con codificación Base64. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Observaciones


Por defecto, las fuentes se escriben en archivos separados. Si esta opción se establece en **true**, las fuentes se incrustarán en el CSS del documento con codificación Base64.

## Ejemplos



Muestra cómo guardar un documento .html con imágenes incrustadas dentro de él.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Muestra cómo incrustar fuentes dentro de un documento HTML guardado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
