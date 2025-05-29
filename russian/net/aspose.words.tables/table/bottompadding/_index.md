---
title: Table.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table BottomPadding, с легкостью настраивайте интервал под содержимым ячеек для улучшенного управления макетом и улучшения визуальной привлекательности.
type: docs
weight: 90
url: /ru/net/aspose.words.tables/table/bottompadding/
---
## Table.BottomPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого под содержимым ячеек.

```csharp
public double BottomPadding { get; set; }
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
