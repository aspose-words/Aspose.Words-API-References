---
title: Table.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: Aspose.Words для .NET
description: Table DistanceRight свойство. Получает или задает расстояние между правой частью таблицы и окружающим текстом в пунктах на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

Получает или задает расстояние между правой частью таблицы и окружающим текстом в пунктах.

```csharp
public double DistanceRight { get; set; }
```

## Примеры

Показывает, как установить расстояние между границами таблицы и текстом.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // Устанавливаем расстояние между таблицей и окружающим текстом.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
