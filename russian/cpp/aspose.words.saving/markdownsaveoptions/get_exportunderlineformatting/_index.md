---
title: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting. Получает или задает логическое значение, указывающее, экспортировать ли подчеркивание текста как последовательность из двух знаков плюса \"++\". Значение по умолчанию — false в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Получает или задает логическое значение, указывающее, экспортировать ли подчеркивание текста как последовательность из двух знаков плюс \"++\". Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Примеры



Показывает, как экспортировать подчеркивание как ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## См. также

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
