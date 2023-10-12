---
title: PreferredWidth.FromPercent
second_title: Справочник по API Aspose.Words для .NET
description: PreferredWidth метод. Метод создания который возвращает новый экземпляр представляющий предпочтительную ширину указанную в процентах.
type: docs
weight: 20
url: /ru/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

Метод создания, который возвращает новый экземпляр, представляющий предпочтительную ширину, указанную в процентах.

```csharp
public static PreferredWidth FromPercent(double percent)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| percent | Double | Значение должно быть от 0 до 100. |

### Примеры

Показывает, как настроить автоматическое размещение таблицы на 50 % ширины страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Показывает, как установить предпочтительную ширину ячеек таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Существует два способа применения класса PreferredWidth к ячейкам таблицы.
// 1 - Установить абсолютную предпочтительную ширину на основе точек:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Установить относительную предпочтительную ширину в процентах от ширины таблицы:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Ячейка, для которой не указана предпочтительная ширина, займет оставшуюся часть доступного пространства.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Каждая конфигурация свойства PreferredWidth создает новый объект.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Смотрите также

* class [PreferredWidth](../)
* пространство имен [Aspose.Words.Tables](../../preferredwidth/)
* сборка [Aspose.Words](../../../)


