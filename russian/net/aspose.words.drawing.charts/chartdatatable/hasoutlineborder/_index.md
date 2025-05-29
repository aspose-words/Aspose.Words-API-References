---
title: ChartDataTable.HasOutlineBorder
linktitle: HasOutlineBorder
articleTitle: HasOutlineBorder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataTable HasOutlineBorder, управляйте отображением границ контура вокруг названий серий и категорий для повышения ясности данных.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartdatatable/hasoutlineborder/
---
## ChartDataTable.HasOutlineBorder property

Возвращает или задает флаг, указывающий, отображается ли граница контура, то есть граница вокруг имен серий и категорий, . Значение по умолчанию:`истинный` .

```csharp
public bool HasOutlineBorder { get; set; }
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

* class [ChartDataTable](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
