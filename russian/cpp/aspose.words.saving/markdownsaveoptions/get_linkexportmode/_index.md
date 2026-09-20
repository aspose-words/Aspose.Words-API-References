---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode метод"
linktitle: "get_LinkExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode метод. Указывает, как ссылки будут записываться в выходной файл. Значение по умолчанию — Auto в C++."
type: docs
weight: 5750
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_linkexportmode/
---
## MarkdownSaveOptions::get_LinkExportMode method


Указывает, как ссылки будут записываться в выходной файл. Значение по умолчанию — [Auto](../../markdownlinkexportmode/).

```cpp
Aspose::Words::Saving::MarkdownLinkExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode() const
```


## Примеры



Показывает, как ссылки будут записаны в файл .md.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 100, 100);

// Изображение будет записано как ссылка:
// ![ref1]
// [ref1]: aw_ref.001.png
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Reference);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Изображение будет записано как встроенное:
// ![](aw_inline.001.png)
saveOptions->set_LinkExportMode(Aspose::Words::Saving::MarkdownLinkExportMode::Inline);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

## См. также

* Enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
