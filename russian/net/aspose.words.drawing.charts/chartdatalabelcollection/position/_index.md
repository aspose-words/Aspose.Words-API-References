---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabelCollection Position, которое позволит легко настраивать позиции меток данных для улучшения визуализации и ясности данных.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Возвращает или задает положение меток данных.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Примечания

Положение можно задать для меток данных следующих типов серий диаграмм:

-Bar ,Column , Histogram ,Pareto , Waterfall ; допустимые значения:Center , InsideBase ,InsideEnd и OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; разрешенные значения:Center ,InsideBase иInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; допустимые значения:Center , Left ,Right , Above иBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; допустимые значения: Center ,InsideEnd , OutsideEnd иBestFit;

-BoxAndWhisker ; допустимые значения: Left ,Right , Above иBelow.

## Примеры

Показывает, как задать положение метки данных.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить столбчатую диаграмму.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Удалить сгенерированную по умолчанию серию.
seriesColl.Clear();

// Добавить серию.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Отображение меток данных и установка цвета шрифта.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Установить позицию метки данных.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Смотрите также

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
