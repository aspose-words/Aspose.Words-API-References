---
title: ChartDataTable.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: Откройте для себя свойство формата ChartDataTable для улучшенного оформления фона текста и границ, что позволит вам улучшить визуализацию данных.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartdatatable/format/
---
## ChartDataTable.Format property

Предоставляет доступ к заполнению фона текста и форматированию границ таблицы данных.

```csharp
public ChartFormat Format { get; }
```

## Примеры

Показывает, как отобразить таблицу данных с данными серии диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

ChartSeriesCollection series = chart.Series;
series.Clear();
double[] xValues = new double[] { 2020, 2021, 2022, 2023 };
series.Add("Series1", xValues, new double[] { 5, 11, 2, 7 });
series.Add("Series2", xValues, new double[] { 6, 5.5, 7, 7.8 });
series.Add("Series3", xValues, new double[] { 10, 8, 7, 9 });

ChartDataTable dataTable = chart.DataTable;
dataTable.Show = true;

dataTable.HasLegendKeys = false;
dataTable.HasHorizontalBorder = false;
dataTable.HasVerticalBorder = false;
dataTable.HasOutlineBorder = false;

dataTable.Font.Italic = true;
dataTable.Format.Stroke.Weight = 1;
dataTable.Format.Stroke.DashStyle = DashStyle.ShortDot;
dataTable.Format.Stroke.Color = Color.DarkBlue;

doc.Save(ArtifactsDir + "Charts.DataTable.docx");
```

### Смотрите также

* class [ChartFormat](../../chartformat/)
* class [ChartDataTable](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
