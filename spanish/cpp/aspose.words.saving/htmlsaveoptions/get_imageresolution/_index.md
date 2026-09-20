---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution método"
linktitle: "get_ImageResolution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution método. Especifica la resolución de salida para imágenes al exportar a HTML, MHTML o EPUB. El valor predeterminado es %96 dpi en C++."
type: docs
weight: 36000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Especifica la resolución de salida para imágenes al exportar a HTML, MHTML o EPUB. El valor predeterminado es **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Observaciones


Esta propiedad afecta a las imágenes raster cuando [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) es **true** y afecta a los metarchivos exportados como imágenes raster. Algunas propiedades de la imagen, como el recorte o la rotación, requieren guardar imágenes transformadas y, en este caso, las imágenes transformadas se crean con la resolución especificada.

## Ejemplos



Muestra cómo establecer carpetas y alias de carpetas para los recursos guardados externamente que Aspose.Words creará al guardar un documento en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
