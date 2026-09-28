---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias метод"
linktitle: "get_ImagesFolderAlias"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias. Указывает имя папки, используемой для построения URI изображений, записываемых в HTML‑документ. По умолчанию это пустая строка в C++."
type: docs
weight: 39000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


Указывает имя папки, используемой для построения URI изображений, записываемых в HTML‑документ. По умолчанию пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Примечания


Когда вы сохраняете [Документ](../../../aspose.words/document/) в формате HTML, Aspose.Words необходимо сохранить все изображения, встроенные в документ, как отдельные файлы. [ImagesFolder](../get_imagesfolder/) позволяет указать, где будут сохраняться изображения, а [ImagesFolderAlias](./) позволяет задать, как будут формироваться URI изображений.

Если [ImagesFolderAlias](./) не является пустой строкой, то URI изображения, записываемый в HTML, будет *ImagesFolderAlias + <image file name>*.

Если [ImagesFolderAlias](./) является пустой строкой, то URI изображения, записываемый в HTML, будет *ImagesFolder + <image file name>*.

Если [ImagesFolderAlias](./) установлен в '.' (точка), то имя файла изображения будет записано в HTML без пути независимо от других параметров.

Альтернативный способ указать имя папки для построения URI изображений — использовать [ResourceFolderAlias](../get_resourcefolderalias/).

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
