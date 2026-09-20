---
title: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution"
linktitle: "get_ImageResolution"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution. Указывает выходное разрешение изображений при экспорте в Markdown. По умолчанию %96 dpi на C++."
type: docs
weight: 3750
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Указывает разрешение вывода изображений при экспорте в Markdown. По умолчанию — **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Примеры



Показывает, как установить выходное разрешение изображений.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## См. также

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
