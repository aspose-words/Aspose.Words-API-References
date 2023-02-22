---
title: Table.DistanceBottom
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает расстояние между нижней частью таблицы и окружающим текстом в пунктах.
type: docs
weight: 120
url: /ru/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Получает расстояние между нижней частью таблицы и окружающим текстом в пунктах.

```csharp
public double DistanceBottom { get; }
```

### Примеры

Показывает операции минимального расстояния между границами таблицы и текстом.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


