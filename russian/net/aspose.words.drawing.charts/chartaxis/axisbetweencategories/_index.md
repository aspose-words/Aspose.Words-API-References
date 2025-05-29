---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartAxis AxisBetweenCategories — управляйте позиционированием оси значений для улучшенной визуализации категорий в ваших диаграммах. Оптимизируйте представление данных!
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Возвращает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Примечания

Свойство действует только для осей значений. Оно не поддерживается новыми диаграммами MS Office 2016.

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
