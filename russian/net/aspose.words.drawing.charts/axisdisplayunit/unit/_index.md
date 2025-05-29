---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AxisDisplayUnit, позволяющее легко настраивать масштабирование единиц отображения с помощью предопределенных значений для улучшенной визуализации данных.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

Возвращает или задает значение масштабирования единиц отображения как одно из предопределенных значений.

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## Примечания

Значение по умолчанию:None .Custom и Percentage значения недоступны в некоторых типах диаграмм; см. [`AxisBuiltInUnit`](../../axisbuiltinunit/) для получения дополнительной информации.

## Примеры

Показывает, как манипулировать делениями и отображаемыми значениями осей диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Установите малые деления оси Y так, чтобы они указывали в сторону от области графика,
// и основные деления, пересекающие ось.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Установите ось Y так, чтобы она отображала основную метку каждые 10 единиц, а второстепенную — каждую 1 единицу.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Установите границы оси Y на -10 и 20.
// Теперь на этой оси Y будут отображаться 4 основных и 27 второстепенных делений.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Для оси X установите основные деления через каждые 10 единиц,
// каждое незначительное деление на 2,5 единицы.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Настройте оба типа делений для отображения внутри области построения графика.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Установите границы оси X так, чтобы ось X охватывала 5 основных делений и 12 второстепенных делений.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Установите метки делений так, чтобы они отображали их значение в миллионах.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Мы можем задать более конкретное значение, по которому метки делений будут отображать свои значения.
// Это утверждение эквивалентно приведенному выше.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Смотрите также

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
