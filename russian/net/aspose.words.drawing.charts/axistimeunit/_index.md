---
title: AxisTimeUnit Enum
linktitle: AxisTimeUnit
articleTitle: AxisTimeUnit
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.Charts.AxisTimeUnit — ваше решение для эффективного и действенного определения единиц времени на осях диаграммы.
type: docs
weight: 860
url: /ru/net/aspose.words.drawing.charts/axistimeunit/
---
## AxisTimeUnit enumeration

Указывает единицу времени для осей.

```csharp
public enum AxisTimeUnit
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Automatic | `0` | Указывает, что единица измерения не была задана явно и следует использовать значение по умолчанию. |
| Days | `1` | Указывает, что данные диаграммы должны отображаться в днях. |
| Months | `2` | Указывает, что данные диаграммы должны отображаться в месяцах. |
| Years | `3` | Указывает, что данные диаграммы должны отображаться в годах. |

## Примеры

Показывает, как вставить диаграмму со значениями даты/времени.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Добавить пользовательскую серию, содержащую значения даты/времени для оси X и соответствующие десятичные значения для оси Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Устанавливаем нижнюю и верхнюю границы для оси X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Установите основные единицы оси X на неделю, а второстепенные единицы — на день.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Определить свойства оси Y для десятичных значений.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
