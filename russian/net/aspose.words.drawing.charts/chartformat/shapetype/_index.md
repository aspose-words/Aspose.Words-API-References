---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: Aspose.Words для .NET
description: ChartFormat ShapeType свойство. Получает или задает тип фигуры родительского элемента диаграммы на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

Получает или задает тип фигуры родительского элемента диаграммы.

```csharp
public ChartShapeType ShapeType { get; set; }
```

## Примечания

В настоящее время это свойство можно использовать только для меток данных.

## Примеры

Показывает, как настроить форматирование заливки, обводки и выносок для меток данных диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Удалить созданную по умолчанию серию.
chart.Series.Clear();

// Добавляем новую серию.
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// Показ меток данных.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// Форматируем метки данных как выноски.
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

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
