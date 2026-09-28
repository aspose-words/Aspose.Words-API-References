---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml метод"
linktitle: "get_ExportAsHtml"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml метод. Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML. Значение по умолчанию — None в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML. Значение по умолчанию — [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


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

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
