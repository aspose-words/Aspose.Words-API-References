---
title: AxisBound.IsAuto
linktitle: IsAuto
articleTitle: IsAuto
second_title: Aspose.Words для .NET
description: AxisBound IsAuto свойство. Возвращает флаг указывающий что граница оси должна определяться автоматически на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/axisbound/isauto/
---
## AxisBound.IsAuto property

Возвращает флаг, указывающий, что граница оси должна определяться автоматически.

```csharp
public bool IsAuto { get; }
```

## Примеры

Показывает, как установить пользовательские границы оси.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Добавляем серию с двумя десятичными массивами. Первый массив содержит значения X,
// а второй содержит соответствующие значения Y для точек точечной диаграммы.
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// По умолчанию масштабирование по умолчанию применяется к осям X и Y графика,
// так, чтобы оба их диапазона были достаточно большими, чтобы охватить все значения X и Y каждой серии.
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// Мы можем определить границы нашей собственной оси.
// В этом случае мы заставим линейки осей X и Y показывать диапазон от 0 до 10.
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// Создайте линейную диаграмму с серией, требующей диапазона дат по оси X и десятичных значений по оси Y.
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// Мы также можем установить границы оси в виде дат, ограничивая диаграмму периодом.
// Установка диапазона 1980-1990 приведет к исключению двух значений ряда
// которые находятся за пределами диапазона графика.
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### Смотрите также

* class [AxisBound](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
