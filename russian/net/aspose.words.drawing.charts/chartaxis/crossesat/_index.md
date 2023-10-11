---
title: ChartAxis.CrossesAt
second_title: Справочник по API Aspose.Words для .NET
description: ChartAxis свойство. Указывает где на перпендикулярной оси пересекается ось.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Указывает, где на перпендикулярной оси пересекается ось.

```csharp
public double CrossesAt { get; set; }
```

### Примечания

Свойство имеет силу только в том случае, если[`Crosses`](../crosses/) настроены наCustom. Не поддерживается новыми диаграммами MS Office 2016.

Единицы измерения определяются типом оси. Если ось является осью значений, значение свойства представляет собой десятичное число на оси значений. Если ось является осью категории времени, значение определяется как целое число дней относительно базовой даты (30.12.1899). Для оси текстовых категорий значение is представляет собой целочисленный номер категории, начиная с 1 в качестве первой категории.

### Примеры

Показывает, как заставить ось графика пересекаться в произвольном месте.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Для столбчатых диаграмм ось Y по умолчанию пересекает нулевую точку,
// это означает, что столбцы для всех значений ниже нуля указывают вниз, обозначая отрицательные значения.
// Мы можем установить другое значение для пересечения оси Y. В данном случае мы установим значение 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Смотрите также

* class [ChartAxis](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartaxis/)
* сборка [Aspose.Words](../../../)


