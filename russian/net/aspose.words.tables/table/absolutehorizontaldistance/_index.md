---
title: Table.AbsoluteHorizontalDistance
linktitle: AbsoluteHorizontalDistance
articleTitle: AbsoluteHorizontalDistance
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table AbsoluteHorizontalDistance, чтобы легко настроить горизонтальное положение таблицы в точках. Оптимизируйте макет со значением по умолчанию 0!
type: docs
weight: 20
url: /ru/net/aspose.words.tables/table/absolutehorizontaldistance/
---
## Table.AbsoluteHorizontalDistance property

Возвращает или задает абсолютное горизонтальное положение плавающей таблицы, указанное свойствами таблицы, в пунктах. Значение по умолчанию — 0.

```csharp
public double AbsoluteHorizontalDistance { get; set; }
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

// Задайте местоположение таблицы на странице, например, в данном случае в правом нижнем углу.
table.RelativeVerticalAlignment = VerticalAlignment.Bottom;
table.RelativeHorizontalAlignment = HorizontalAlignment.Right;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Table 2, cell 1");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

 // Мы также можем задать горизонтальное и вертикальное смещение в пунктах от местоположения абзаца, куда мы вставили таблицу.
table.AbsoluteVerticalDistance = 50;
table.AbsoluteHorizontalDistance = 100;

doc.Save(ArtifactsDir + "Table.ChangeFloatingTableProperties.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
