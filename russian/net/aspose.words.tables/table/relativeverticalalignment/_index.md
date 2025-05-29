---
title: Table.RelativeVerticalAlignment
linktitle: RelativeVerticalAlignment
articleTitle: RelativeVerticalAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Table RelativeVerticalAlignment, которое позволяет легко управлять вертикальным выравниванием плавающих таблиц, повышая точность и дизайн вашего макета.
type: docs
weight: 240
url: /ru/net/aspose.words.tables/table/relativeverticalalignment/
---
## Table.RelativeVerticalAlignment property

Возвращает или задает относительное вертикальное выравнивание плавающей таблицы.

```csharp
public VerticalAlignment RelativeVerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
