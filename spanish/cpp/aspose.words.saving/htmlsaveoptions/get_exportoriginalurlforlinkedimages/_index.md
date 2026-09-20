---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages método"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages método. Especifica si la URL original debe usarse como la URL de las imágenes vinculadas. El valor predeterminado es false en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Especifica si la URL original debe usarse como la URL de las imágenes vinculadas. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Observaciones


Si el valor se establece en **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) el valor se usa como la URL de las imágenes vinculadas y las imágenes vinculadas no se cargan en la carpeta del documento o en [ImagesFolder](../get_imagesfolder/).

Si el valor se establece en **false** las imágenes vinculadas se cargan en la carpeta del documento o en [ImagesFolder](../get_imagesfolder/) y la URL de cada imagen vinculada se construye en función de la carpeta del documento, [ImagesFolder](../get_imagesfolder/) y las propiedades [ImagesFolderAlias](../get_imagesfolderalias/).

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
