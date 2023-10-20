---
title: ChartDataLabelCollection.ShowPercentage
linktitle: ShowPercentage
articleTitle: ShowPercentage
second_title: Aspose.Words для .NET
description: ChartDataLabelCollection ShowPercentage свойство. Позволяет указать должно ли отображаться процентное значение для меток данных всей серии. Значение по умолчаниюЛОЖЬ . Применяется только к круговым диаграммам на С#.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/
---
## ChartDataLabelCollection.ShowPercentage property

Позволяет указать, должно ли отображаться процентное значение для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . Применяется только к круговым диаграммам.

```csharp
public bool ShowPercentage { get; set; }
```

## Примечания

Значение, определенное для этого свойства, можно переопределить для отдельной метки данных с помощью the [`ShowPercentage`](../../chartdatalabel/showpercentage/) свойство.

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
