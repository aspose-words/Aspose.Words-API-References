---
title: Table.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words для .NET
description: Table StyleIdentifier свойство. Получает или задает независимый от локали идентификатор стиля таблицы примененный к этой таблице на С#.
type: docs
weight: 280
url: /ru/net/aspose.words.tables/table/styleidentifier/
---
## Table.StyleIdentifier property

Получает или задает независимый от локали идентификатор стиля таблицы, примененный к этой таблице.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Примеры

Показывает, как построить новую таблицу с применением стиля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Мы должны вставить хотя бы одну строку, прежде чем устанавливать какое-либо форматирование таблицы.
builder.InsertCell();

// Установите используемый стиль таблицы на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формате .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Частично применить стиль к функциям таблицы на основе предикатов, затем построить таблицу.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
