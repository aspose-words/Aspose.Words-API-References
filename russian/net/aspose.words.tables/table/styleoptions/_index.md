---
title: Table.StyleOptions
linktitle: StyleOptions
articleTitle: StyleOptions
second_title: Aspose.Words для .NET
description: Table StyleOptions свойство. Получает или устанавливает битовые флаги определяющие как стиль таблицы применяется к этой таблице на С#.
type: docs
weight: 300
url: /ru/net/aspose.words.tables/table/styleoptions/
---
## Table.StyleOptions property

Получает или устанавливает битовые флаги, определяющие, как стиль таблицы применяется к этой таблице.

```csharp
public TableStyleOptions StyleOptions { get; set; }
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

* enum [TableStyleOptions](../../tablestyleoptions/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
