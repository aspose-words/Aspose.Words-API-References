---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words для .NET
description: ChartDataLabelCollection ShowLeaderLines свойство. Позволяет указать нужно ли отображать выносные линии меток данных для меток данных всей серии. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 100
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

Позволяет указать, нужно ли отображать выносные линии меток данных для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## Примечания

Применяется только к круговым диаграммам. Линии-выноски создают визуальную связь между меткой данных и соответствующей точкой данных.

Значение, определенное для этого свойства, можно переопределить для отдельной метки данных с помощью the .[`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) свойство.

## Примеры

Показывает, как работать с метками данных на круговой диаграмме.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставляем пользовательскую серию диаграмм с именем категории для каждого сектора и их таблицей частот.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Включите метки данных, которые будут отображать процент и частоту каждого сектора, и измените их внешний вид.
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
