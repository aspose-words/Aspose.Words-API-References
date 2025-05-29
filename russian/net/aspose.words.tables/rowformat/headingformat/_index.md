---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RowFormat HeadingFormat, гарантируйте, что заголовки таблиц повторяются на каждой странице для ясности и улучшения читаемости многостраничных документов.
type: docs
weight: 30
url: /ru/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Истина, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы.

```csharp
public bool HeadingFormat { get; set; }
```

## Примеры

Показывает, как построить таблицу со строками, повторяющимися на каждой странице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Любые строки, вставленные, когда флаг "HeadingFormat" установлен в значение "true"
// будет отображаться в верхней части таблицы на каждой странице, которую он занимает.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Добавьте достаточно строк, чтобы таблица заняла две страницы.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Смотрите также

* class [RowFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
