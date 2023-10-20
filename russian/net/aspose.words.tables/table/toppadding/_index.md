---
title: Table.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words для .NET
description: Table TopPadding свойство. Получает или задает объем пространства в пунктах добавляемого над содержимым ячеек на С#.
type: docs
weight: 330
url: /ru/net/aspose.words.tables/table/toppadding/
---
## Table.TopPadding property

Получает или задает объем пространства (в пунктах), добавляемого над содержимым ячеек.

```csharp
public double TopPadding { get; set; }
```

## Примеры

Показывает, как настроить заполнение содержимого в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndTable();

 // Для каждой ячейки таблицы задаем расстояние между ее содержимым и каждой из ее границ.
// Эта таблица будет поддерживать минимальное расстояние заполнения путем переноса текста.
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
