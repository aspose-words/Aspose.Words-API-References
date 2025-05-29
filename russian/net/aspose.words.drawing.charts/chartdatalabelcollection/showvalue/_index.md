---
title: ChartDataLabelCollection.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ShowValue в ChartDataLabelCollection улучшает визуализацию данных, отображая значения серий. Оптимизируйте свои диаграммы сегодня!
type: docs
weight: 170
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/showvalue/
---
## ChartDataLabelCollection.ShowValue property

Позволяет указать, будут ли значения отображаться в метках данных всей серии. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowValue { get; set; }
```

## Примечания

Значение, определенное для этого свойства, может быть переопределено для отдельной метки данных с помощью [`ShowValue`](../../chartdatalabel/showvalue/) свойство.

## Примеры

Показывает, как работать с метками данных круговой диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставьте пользовательскую серию диаграмм с названием категории для каждого из секторов и их таблицей частот.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Включить метки данных, которые будут отображать как процент, так и частоту каждого сектора, и изменить их внешний вид.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Смотрите также

* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
