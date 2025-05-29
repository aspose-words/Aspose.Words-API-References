---
title: ChartDataLabelCollection.Separator
linktitle: Separator
articleTitle: Separator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Separator ChartDataLabelCollection. Настройте разделители меток данных для большей ясности в ваших диаграммах, от запятых до переносов строк.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Возвращает или задает разделитель строк, используемый для меток данных всей серии. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процент, когда вместо этого следует использовать разрыв строки .

```csharp
public string Separator { get; set; }
```

## Примечания

Значение, определенное для этого свойства, может быть переопределено для отдельной метки данных с помощью [`Separator`](../../chartdatalabel/separator/) свойство.

## Примеры

Показывает, как работать с метками данных пузырьковой диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

 // Добавьте пользовательскую серию с координатами X/Y и диаметром каждого из пузырьков.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Включите метки данных, а затем измените их внешний вид.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

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
