---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup DoughnutHoleSize, чтобы легко настроить процент размера отверстия кольцевой диаграммы для улучшенной визуализации данных.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

Возвращает или задает размер отверстия родительской кольцевой диаграммы в процентах.

```csharp
public int DoughnutHoleSize { get; set; }
```

## Примечания

Применимо только к группам серийDoughnut тип.

Диапазон допустимых значений — от 0 до 90 включительно. Значение по умолчанию — 75.

## Примеры

Показывает, как создать и отформатировать кольцевую диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

// Форматируем кольцевую диаграмму.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### Смотрите также

* class [ChartSeriesGroup](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
