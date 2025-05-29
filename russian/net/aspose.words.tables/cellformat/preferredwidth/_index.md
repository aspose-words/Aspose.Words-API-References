---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat PreferredWidth, чтобы легко настраивать ширину ячеек для оптимального макета и дизайна в ваших электронных таблицах. Улучшите представление данных!
type: docs
weight: 80
url: /ru/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Возвращает или задает предпочтительную ширину ячейки.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Примечания

Предпочтительная ширина (вместе с опцией таблицы Auto Fit) определяет, как фактическая ширина ячейки рассчитывается алгоритмом макета таблицы. Макет таблицы может быть выполнен Aspose.Words при сохранении документа или Microsoft Word при отображении документа.

Предпочтительная ширина может быть указана в пунктах или процентах. Предпочтительная ширина также может быть указана как «auto», что означает, что предпочтительная ширина не указана.

Значение по умолчанию:[`Auto`](../../preferredwidth/auto/).

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
