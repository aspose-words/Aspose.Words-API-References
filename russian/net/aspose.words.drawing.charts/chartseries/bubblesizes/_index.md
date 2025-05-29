---
title: ChartSeries.BubbleSizes
linktitle: BubbleSizes
articleTitle: BubbleSizes
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries BubbleSizes, чтобы получить доступ к настраиваемым размерам пузырьков, что улучшит визуализацию данных и построение диаграмм.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartseries/bubblesizes/
---
## ChartSeries.BubbleSizes property

Получает коллекцию размеров пузырьков для этой серии диаграмм.

```csharp
public BubbleSizeCollection BubbleSizes { get; }
```

## Примеры

Показывает, как работать с кодом формата данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте пузырьковую диаграмму.
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// Установить коды формата данных.
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### Смотрите также

* class [BubbleSizeCollection](../../bubblesizecollection/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
