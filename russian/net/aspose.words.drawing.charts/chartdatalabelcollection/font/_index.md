---
title: ChartDataLabelCollection.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Получите доступ и настройте форматирование шрифта для всех меток данных вашей серии с помощью свойства шрифта ChartDataLabelCollection для улучшенной визуализации данных.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---
## ChartDataLabelCollection.Font property

Предоставляет доступ к форматированию шрифта меток данных всей серии.

```csharp
public Font Font { get; }
```

## Примечания

Значение, определенное для этого свойства, может быть переопределено для отдельной метки данных с помощью [`Font`](../../chartdatalabel/font/) свойство.

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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
