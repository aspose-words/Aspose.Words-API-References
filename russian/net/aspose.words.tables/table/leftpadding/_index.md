---
title: Table.LeftPadding
linktitle: LeftPadding
articleTitle: LeftPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table LeftPadding, легко настройте интервал между содержимым ячеек в пунктах для улучшенного управления макетом и повышения гибкости дизайна.
type: docs
weight: 200
url: /ru/net/aspose.words.tables/table/leftpadding/
---
## Table.LeftPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого слева от содержимого ячеек.

```csharp
public double LeftPadding { get; set; }
```

## Примеры

Показывает, как настроить отступы для содержимого в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Для каждой ячейки таблицы задайте расстояние между ее содержимым и каждой из ее границ.
// Эта таблица будет поддерживать минимальное расстояние отступа путем переноса текста.
table.LeftPadding = 30;
table.RightPadding = 60;
table.TopPadding = 10;
table.BottomPadding = 90;
table.PreferredWidth = PreferredWidth.FromPoints(250);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
