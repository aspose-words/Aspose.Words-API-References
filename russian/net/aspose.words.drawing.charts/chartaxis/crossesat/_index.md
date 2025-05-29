---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartAxis CrossesAt, позволяющее легко определять точки пересечения на перпендикулярной оси диаграммы для улучшенной визуализации данных.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Указывает, где на перпендикулярной оси пересекается ось.

```csharp
public double CrossesAt { get; set; }
```

## Примечания

Свойство имеет силу только в том случае, если[`Crosses`](../crosses/) установлены наCustom. Не поддерживается новыми диаграммами MS Office 2016.

Единицы определяются типом оси. Если ось является осью значений, значение свойства является десятичным числом на оси значений. Если ось является осью категории времени, значение определяется как целое число дней относительно базовой даты (30/12/1899). Для оси текстовой категории значением является целое число категории, начиная с 1 в качестве первой категории.

## Примеры

Показывает, как сделать так, чтобы ось графика пересекалась в заданном месте.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Для столбчатых диаграмм ось Y по умолчанию пересекается в нуле,
// что означает, что столбцы для всех значений ниже нуля направлены вниз, представляя отрицательные значения.
// Мы можем задать другое значение для пересечения оси Y. В этом случае мы установим его на 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Смотрите также

* class [ChartAxis](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
