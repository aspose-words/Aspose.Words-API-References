---
title: ChartDataLabelCollection.ShowLegendKey
second_title: Справочник по API Aspose.Words для .NET
description: ChartDataLabelCollection свойство. Позволяет указать должен ли отображаться ключ легенды для меток данных всей серии. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 110
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/
---
## ChartDataLabelCollection.ShowLegendKey property

Позволяет указать, должен ли отображаться ключ легенды для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowLegendKey { get; set; }
```

### Примечания

Значение, определенное для этого свойства, можно переопределить для отдельной метки данных с помощью the [`ShowLegendKey`](../../chartdatalabel/showlegendkey/) свойство.

### Примеры

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
* пространство имен [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* сборка [Aspose.Words](../../../)


