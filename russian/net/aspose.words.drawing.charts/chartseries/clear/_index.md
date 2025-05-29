---
title: ChartSeries.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words для .NET
description: Оптимизируйте свои диаграммы с помощью метода ChartSeries Clear! Легко удаляйте значения данных и сбрасывайте форматирование для более чистого и профессионального вида.
type: docs
weight: 170
url: /ru/net/aspose.words.drawing.charts/chartseries/clear/
---
## ChartSeries.Clear method

Удаляет все значения данных из серии диаграмм. Формат всех отдельных точек данных и меток данных очищается.

```csharp
public void Clear()
```

## Примеры

Показывает, как заполнить ряды диаграмм данными.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Очистить значения X и Y первой серии.
series1.ClearValues();

// Заполняем ряд данными.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Очистить значения X и Y второй серии.
series2.Clear();

// Заполняем ряд данными.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Смотрите также

* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
