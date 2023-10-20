---
title: ChartDataLabelCollection.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words для .NET
description: ChartDataLabelCollection NumberFormat свойство. ПолучаетChartNumberFormat экземпляр позволяющий установить числовой формат для меток данных всей серии  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/numberformat/
---
## ChartDataLabelCollection.NumberFormat property

Получает[`ChartNumberFormat`](../../chartnumberformat/) экземпляр, позволяющий установить числовой формат для меток данных всей серии .

```csharp
public ChartNumberFormat NumberFormat { get; }
```

## Примеры

Показывает, как включить и настроить метки данных для серии диаграмм.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем линейный график, затем очищаем серию демонстрационных данных, чтобы начать с чистого графика,
// а затем задаем заголовок.
Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;
chart.Series.Clear();
chart.Title.Text = "Monthly sales report";

// Вставляем пользовательскую серию диаграмм с месяцами в качестве категорий для оси X,
// и соответствующие десятичные суммы для оси Y.
ChartSeries series = chart.Series.Add("Revenue", 
    new[] { "January", "February", "March" }, 
    new[] { 25.611d, 21.439d, 33.750d });

// Включите метки данных, а затем примените собственный числовой формат для значений, отображаемых в метках данных.
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
