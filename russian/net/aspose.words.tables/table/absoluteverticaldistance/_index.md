---
title: Table.AbsoluteVerticalDistance
linktitle: AbsoluteVerticalDistance
articleTitle: AbsoluteVerticalDistance
second_title: Aspose.Words для .NET
description: Table AbsoluteVerticalDistance свойство. Получает или задает абсолютное вертикальное плавающее положение таблицы указанное в свойствах таблицы в точках. Значение по умолчанию  0 на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.tables/table/absoluteverticaldistance/
---
## Table.AbsoluteVerticalDistance property

Получает или задает абсолютное вертикальное плавающее положение таблицы, указанное в свойствах таблицы, в точках. Значение по умолчанию — 0.

```csharp
public double AbsoluteVerticalDistance { get; set; }
```

## Примеры

Показывает, как задать расположение плавающих таблиц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 1, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

// Установите местоположение таблицы в нужном месте на странице, например, в данном случае в правом нижнем углу.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Мы также можем установить горизонтальное и вертикальное смещение в пунктах от места абзаца, куда мы вставили таблицу.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
