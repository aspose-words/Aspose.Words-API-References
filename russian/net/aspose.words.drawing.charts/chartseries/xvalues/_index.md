---
title: ChartSeries.XValues
linktitle: XValues
articleTitle: XValues
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries XValues, чтобы получить доступ к мощной коллекции значений X, улучшающей визуализацию и анализ данных.
type: docs
weight: 140
url: /ru/net/aspose.words.drawing.charts/chartseries/xvalues/
---
## ChartSeries.XValues property

Получает коллекцию значений X для этой серии диаграмм.

```csharp
public ChartXValueCollection XValues { get; }
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

* class [ChartXValueCollection](../../chartxvaluecollection/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
