---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabelCollection NumberFormat, которое позволяет легко настраивать форматы меток данных для всей серии, повышая ясность и наглядность.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Получает[`ChartNumberFormat`](../../chartnumberformat/) экземпляр, позволяющий задать числовой формат для меток данных всей серии x000d_.

```csharp
public ChartNumberFormat NumberFormat { get; }
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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
