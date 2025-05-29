---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.MarkdownExportAsHtml, чтобы легко преобразовывать элементы Markdown в необработанный HTML, расширяя возможности экспорта документов.
type: docs
weight: 6020
url: /ru/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Экспортировать все элементы, используя синтаксис Markdown без какого-либо необработанного HTML. |
| Tables | `1` | Экспортировать таблицы как необработанный HTML. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
