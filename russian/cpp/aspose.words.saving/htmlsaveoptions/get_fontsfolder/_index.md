---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder метод"
linktitle: "get_FontsFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder метод. Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию это пустая строка в C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Указывает физическую папку, в которой шрифты сохраняются при экспорте документа в HTML. По умолчанию пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате HTML и параметр [ExportFontResources](../get_exportfontresources/) установлен в **true**, Aspose.Words необходимо сохранять шрифты, используемые в документе, как отдельные файлы. [FontsFolder](./) позволяет указать, где будут сохраняться шрифты, а [FontsFolderAlias](../get_fontsfolderalias/) позволяет задать, как будут построены URI шрифтов.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет шрифты в той же папке, где сохранён файл документа. Используйте [FontsFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения шрифтов, но всё равно необходимо где‑то их сохранить. В этом случае нужно указать доступную папку в свойстве [FontsFolder](./) или предоставить пользовательские потоки через обработчик события [FontSavingCallback](../get_fontsavingcallback/).

Если папка, указанная в [FontsFolder](./), не существует, она будет создана автоматически.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
