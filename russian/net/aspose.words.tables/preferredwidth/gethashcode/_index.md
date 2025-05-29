---
title: PreferredWidth.GetHashCode
linktitle: GetHashCode
articleTitle: GetHashCode
second_title: Aspose.Words для .NET
description: Откройте для себя метод PreferredWidth GetHashCode — важную хэш-функцию для эффективной обработки данных и генерации уникальных значений в ваших приложениях.
type: docs
weight: 70
url: /ru/net/aspose.words.tables/preferredwidth/gethashcode/
---
## PreferredWidth.GetHashCode method

Служит хэш-функцией для этого типа.

```csharp
public override int GetHashCode()
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
