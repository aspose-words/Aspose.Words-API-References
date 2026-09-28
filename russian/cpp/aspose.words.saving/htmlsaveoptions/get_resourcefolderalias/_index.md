---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias метод"
linktitle: "get_ResourceFolderAlias"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias метод. Указывает имя папки, используемой для построения URI всех ресурсов, записываемых в HTML‑документ. По умолчанию в C++ это пустая строка."
type: docs
weight: 44000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolderalias/
---
## HtmlSaveOptions::get_ResourceFolderAlias method


Указывает имя папки, используемой для построения URI всех ресурсов, записываемых в HTML‑документ. По умолчанию это пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias() const
```

## Примечания


[ResourceFolderAlias](./) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [ImagesFolderAlias](../get_imagesfolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) properties, respectively. However, there is no individual property for CSS.

[ResourceFolderAlias](./) has lower priority than [FontsFolderAlias](../get_fontsfolderalias/) and [ImagesFolderAlias](../get_imagesfolderalias/). For example, if both [ResourceFolderAlias](./) and [FontsFolderAlias](../get_fontsfolderalias/) are specified, fonts' URIs will be constructed using [FontsFolderAlias](../get_fontsfolderalias/), while URIs of images and CSS will be constructed using [ResourceFolderAlias](./).

Если [ResourceFolderAlias](./) пустой, будет использовано значение свойства [ResourceFolder](../get_resourcefolder/) для построения URI ресурсов.

Если [ResourceFolderAlias](./) установлен в '.' (точка), URI ресурсов будут содержать только имена файлов без пути.

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
