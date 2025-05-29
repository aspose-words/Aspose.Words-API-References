---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MarkdownSaveOptions ExportAsHtml позволяет вам настраивать элементы HTML для бесшовного экспорта Markdown. Увеличьте универсальность вашего контента!
type: docs
weight: 30
url: /ru/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML. Значение по умолчанию:None .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Примеры

Показывает, как экспортировать таблицу в Markdown как необработанный HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Создать таблицу.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### Смотрите также

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
