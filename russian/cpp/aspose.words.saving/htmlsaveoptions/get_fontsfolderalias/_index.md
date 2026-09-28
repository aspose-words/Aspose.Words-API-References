---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias метод"
linktitle: "get_FontsFolderAlias"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias метод. Указывает имя папки, используемой для построения URI шрифтов, записываемых в HTML‑документ. По умолчанию это пустая строка в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Указывает имя папки, используемой для построения URI шрифтов, записываемых в HTML‑документ. По умолчанию пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате HTML и параметр [ExportFontResources](../get_exportfontresources/) установлен в **true**, Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. [FontsFolder](../get_fontsfolder/) позволяет указать, где будут сохраняться шрифты, а [FontsFolderAlias](./) позволяет задать, как будут построены URI шрифтов.

Если [FontsFolderAlias](./) не является пустой строкой, то URI шрифта, записанный в HTML, будет *FontsFolderAlias + <font file name>*.

Если [FontsFolderAlias](./) является пустой строкой, то URI шрифта, записанный в HTML, будет *FontsFolder + <font file name>*.

Если [FontsFolderAlias](./) установлен в '.' (точка), то имя файла шрифта будет записано в HTML без пути независимо от других параметров.

Альтернативный способ указать имя папки для построения URI шрифтов — использовать [ResourceFolderAlias](../get_resourcefolderalias/).

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
