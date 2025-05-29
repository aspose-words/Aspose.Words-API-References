---
title: ChartSeries.HasDataLabels
linktitle: HasDataLabels
articleTitle: HasDataLabels
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries HasDataLabels, которое позволяет легко управлять видимостью меток данных для ваших серий, улучшая процесс визуализации данных.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing.charts/chartseries/hasdatalabels/
---
## ChartSeries.HasDataLabels property

Возвращает или задает флаг, указывающий, отображаются ли метки данных для серии.

```csharp
public bool HasDataLabels { get; set; }
```

## Примеры

Показывает, как включить и настроить метки данных для серии диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте линейный график, затем очистите его серию демонстрационных данных, чтобы начать с чистого графика,
// а затем задайте заголовок.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Вставьте пользовательскую серию диаграмм с месяцами в качестве категорий для оси X,
// и соответствующие десятичные значения для оси Y.
ChartSeries series = chart.Series.Add("Revenue",
    new[] { "January", "February", "March" },
    new[] { 25.611d, 21.439d, 33.750d });

// Включите метки данных, а затем примените пользовательский числовой формат для значений, отображаемых в метках данных.
// Этот формат будет обрабатывать отображаемые десятичные значения как миллионы долларов США.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.NumberFormat.FormatCode = "\"US$\" #,##0.000\"M\"";
dataLabels.Font.Size = 12;

doc.Save(ArtifactsDir + "Charts.DataLabelNumberFormat.docx");
```

### Смотрите также

* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
