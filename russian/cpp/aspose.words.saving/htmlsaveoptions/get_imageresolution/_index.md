---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution метод"
linktitle: "get_ImageResolution"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution метод. Указывает разрешение вывода для изображений при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — %96 dpi в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Указывает разрешение вывода изображений при экспорте в HTML, MHTML или EPUB. По умолчанию **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Примечания


Это свойство влияет на растровые изображения, когда [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) **true**, и влияет на метафайлы, экспортируемые как растровые изображения. Некоторые свойства изображений, такие как обрезка или вращение, требуют сохранения преобразованных изображений, и в этом случае преобразованные изображения создаются с заданным разрешением.

## Примеры



Показывает, как задавать папки и псевдонимы папок для внешних сохраняемых ресурсов, которые Aspose.Words создаст при сохранении документа в HTML.
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

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
