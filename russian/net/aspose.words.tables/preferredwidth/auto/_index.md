---
title: PreferredWidth.Auto
linktitle: Auto
articleTitle: Auto
second_title: Aspose.Words для .NET
description: Откройте для себя поле PreferredWidth Auto, которое эффективно обрабатывает неуказанные значения ширины для оптимальной настройки макета в ваших проектах.
type: docs
weight: 10
url: /ru/net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

Возвращает экземпляр, представляющий значение «предпочтительная ширина не указана».

```csharp
public static readonly PreferredWidth Auto;
```

## Примеры

Показывает, как установить предпочтительную ширину ячеек таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Существует два способа применения класса «PreferredWidth» к ячейкам таблицы.
// 1 — Установить абсолютную предпочтительную ширину на основе точек:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Установить относительную предпочтительную ширину на основе процента от ширины таблицы:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Ячейка, для которой не указана предпочтительная ширина, займет оставшееся доступное пространство.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Каждая конфигурация свойства «PreferredWidth» создает новый объект.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Смотрите также

* class [PreferredWidth](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
