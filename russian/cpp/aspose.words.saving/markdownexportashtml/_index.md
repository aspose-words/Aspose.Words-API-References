---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enum"
linktitle: "MarkdownExportAsHtml"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownExportAsHtml enum. Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML в C++."
type: docs
weight: 66500
url: /ru/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML.

```cpp
enum class MarkdownExportAsHtml
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Экспортировать все элементы, используя синтаксис Markdown, без какого‑либо необработанного HTML. |
| Таблицы | 1 | Экспортировать таблицы как необработанный HTML. |
| NonCompatibleTables | 2 | Экспортировать таблицы, которые нельзя корректно представить в чистом Markdown, как необработанный HTML. |


## Примеры



Показывает, как экспортировать таблицу в Markdown как необработанный HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Создать таблицу.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
