---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup FirstSliceAngle, позволяющее настроить угол первого сектора круговой диаграммы в градусах для улучшенной визуализации данных.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

Возвращает или задает угол в градусах первого сектора родительской круговой диаграммы.

```csharp
public int FirstSliceAngle { get; set; }
```

## Примечания

Применимо к группам серийPie ,Pie3D иDoughnut типы.

Диапазон допустимых значений — от 0 до 360 включительно. Значение по умолчанию — 0.

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
