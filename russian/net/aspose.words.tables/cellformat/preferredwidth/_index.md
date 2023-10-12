---
title: CellFormat.PreferredWidth
second_title: Справочник по API Aspose.Words для .NET
description: CellFormat свойство. Возвращает или устанавливает предпочтительную ширину ячейки.
type: docs
weight: 80
url: /ru/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Возвращает или устанавливает предпочтительную ширину ячейки.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

### Примечания

Предпочтительная ширина (вместе с параметром «Автоподбор» таблицы) определяет, как фактическая ширина ячейки рассчитывается алгоритмом макета таблицы. Макет таблицы может быть выполнен с помощью Aspose.Words при сохранении документа или с помощью Microsoft Word при отображении документа.

Предпочтительная ширина может быть указана в пунктах или процентах. Предпочтительная ширина также может быть указана как «авто», что означает, что предпочтительная ширина не указана.

Значение по умолчанию:[`Auto`](../../preferredwidth/auto/).

### Примеры

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../cellformat/)
* сборка [Aspose.Words](../../../)


