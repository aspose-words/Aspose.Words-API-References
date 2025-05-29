---
title: ChartDataTable Class
linktitle: ChartDataTable
articleTitle: ChartDataTable
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartDataTable, чтобы легко настраивать таблицы данных диаграмм и улучшать визуализацию данных с помощью мощных функций.
type: docs
weight: 990
url: /ru/net/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class

Позволяет указать свойства таблицы данных диаграммы.

```csharp
public class ChartDataTable
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatatable/font/) { get; } | Предоставляет доступ к форматированию шрифтов таблицы данных. |
| [Format](../../aspose.words.drawing.charts/chartdatatable/format/) { get; } | Предоставляет доступ к заполнению фона текста и форматированию границ таблицы данных. |
| [HasHorizontalBorder](../../aspose.words.drawing.charts/chartdatatable/hashorizontalborder/) { get; set; } | Возвращает или задает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. Значение по умолчанию:`истинный` . |
| [HasLegendKeys](../../aspose.words.drawing.charts/chartdatatable/haslegendkeys/) { get; set; } | Возвращает или задает флаг, указывающий, отображаются ли ключи легенды в таблице данных. Значение по умолчанию:`истинный` . |
| [HasOutlineBorder](../../aspose.words.drawing.charts/chartdatatable/hasoutlineborder/) { get; set; } | Возвращает или задает флаг, указывающий, отображается ли граница контура, то есть граница вокруг имен серий и категорий, . Значение по умолчанию:`истинный` . |
| [HasVerticalBorder](../../aspose.words.drawing.charts/chartdatatable/hasverticalborder/) { get; set; } | Возвращает или задает флаг, указывающий, отображается ли вертикальная граница таблицы данных. Значение по умолчанию:`истинный` . |
| [Show](../../aspose.words.drawing.charts/chartdatatable/show/) { get; set; } | Возвращает или задает флаг, указывающий, будет ли отображаться таблица данных для диаграммы. Значение по умолчанию:`ЛОЖЬ` . |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
