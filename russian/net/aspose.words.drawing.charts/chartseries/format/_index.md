---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeries Format для легкого доступа к настраиваемым стилям заливки и линий, расширяя возможности визуализации данных.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Предоставляет доступ к заполнению и форматированию линий серии.

```csharp
public ChartFormat Format { get; }
```

## Примеры

Рассказывает, как задать цвет серии.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Удалить сгенерированную по умолчанию серию.
seriesColl.Clear();

// Создаем массив названий категорий.
string[] categories = new[] { "Category 1", "Category 2" };

// Добавление новой серии. Массивы значений и категорий должны быть одинакового размера.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Установить цвет серии.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Смотрите также

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
