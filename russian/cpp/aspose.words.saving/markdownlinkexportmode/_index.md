---
title: "Перечисление Aspose::Words::Saving::MarkdownLinkExportMode"
linktitle: "MarkdownLinkExportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Saving::MarkdownLinkExportMode. Указывает, как ссылки экспортируются в Markdown в C++."
type: docs
weight: 67000
url: /ru/cpp/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enum


Указывает, как ссылки экспортируются в Markdown.

```cpp
enum class MarkdownLinkExportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Авто | 0 | Автоматически определять режим экспорта для каждой ссылки. |
| Встроенный | 1 | Экспортировать все ссылки как встроенные блоки. |
| Ссылка | 2 | Экспортировать все ссылки как блоки‑ссылки. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
