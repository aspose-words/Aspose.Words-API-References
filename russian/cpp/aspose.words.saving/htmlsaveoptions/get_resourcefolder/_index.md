---
title: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder"
linktitle: "get_ResourceFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder. Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешние CSS, при экспорте документа в HTML. По умолчанию это пустая строка в C++."
type: docs
weight: 43000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolder/
---
## HtmlSaveOptions::get_ResourceFolder method


Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешние CSS, при экспорте документа в HTML. По умолчанию это пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder() const
```

## Примечания


[ResourceFolder](./) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/).

[ResourceFolder](./) has a lower priority than folders specified via [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/). For example, if both [ResourceFolder](./) and [FontsFolder](../get_fontsfolder/) are specified, fonts will be saved to [FontsFolder](../get_fontsfolder/), while images and CSS will be saved to [ResourceFolder](./).

Если папка, указанная в [ResourceFolder](./), не существует, она будет создана автоматически.

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
