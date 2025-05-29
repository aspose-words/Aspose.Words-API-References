---
title: ChartSeriesGroup.SecondSectionSize
linktitle: SecondSectionSize
articleTitle: SecondSectionSize
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство SecondSectionSize в ChartSeriesGroup, чтобы эффективно настроить размер вторичной секции круговой диаграммы.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/
---
## ChartSeriesGroup.SecondSectionSize property

Возвращает или задает размер вторичной секции круговой диаграммы в процентах.

```csharp
public int SecondSectionSize { get; set; }
```

## Примечания

Применимо к группам серийPieOfPie и PieOfBar типы.

Диапазон допустимых значений — от 5 до 200 включительно. Значение по умолчанию — 75.

## Примеры

Показывает, как создать и отформатировать круговую диаграмму.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.PieOfPie, 440, 300);
Chart chart = shape.Chart;
// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3", "Category 4" };
chart.Series.Add("Series 1", categories, new double[] { 11, 8, 4, 3 });

// Форматируем круговую диаграмму.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.GapWidth = 10;
seriesGroup.SecondSectionSize = 77;

doc.Save(ArtifactsDir + "Charts.PieOfPieChart.docx");
```

### Смотрите также

* class [ChartSeriesGroup](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
