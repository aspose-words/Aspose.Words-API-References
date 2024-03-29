---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: ChartDataPoint Format свойство. Предоставляет доступ к форматированию заливки и строк этой точки данных на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Предоставляет доступ к форматированию заливки и строк этой точки данных.

```csharp
public ChartFormat Format { get; }
```

## Примеры

Показывает, как установить индивидуальное форматирование для категорий гистограммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Удалить созданную по умолчанию серию.
chart.Series.Clear();

// Добавляем новую серию.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Устанавливаем форматирование столбца.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

### Смотрите также

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
