---
title: ChartDataLabelCollection.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabelCollection Format для легкого доступа к настраиваемому форматированию заливки и линий для ваших меток данных. Улучшите свои диаграммы сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/format/
---
## ChartDataLabelCollection.Format property

Предоставляет доступ к заполнению и форматированию строк меток данных.

```csharp
public ChartFormat Format { get; }
```

## Примеры

Показывает, как задать форматирование заливки, обводки и выносок для меток данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();

// Добавить новую серию.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Показать метки данных.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Форматировать метки данных как выноски.
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// Изменить заливку и обводку отдельной метки данных.
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### Смотрите также

* class [ChartFormat](../../chartformat/)
* class [ChartDataLabelCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
