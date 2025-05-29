---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.AxisBound — ваше решение для определения пределов значений осей в диаграммах для точной визуализации данных.
type: docs
weight: 750
url: /ru/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Представляет минимальную или максимальную границу значений оси.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public sealed class AxisBound
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Создает новый экземпляр, указывающий, что граница оси должна определяться автоматически приложением текстового процессора . |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Создает границу оси, представленную как значение datetime. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Создает границу оси, представленную числом. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Возвращает флаг, указывающий, что граница оси должна быть определена автоматически. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Возвращает числовое значение границы оси. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Возвращает значение границы оси, представленное как datetime. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Определяет, равен ли указанный объект по значению текущему объекту. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Служит хэш-функцией для этого типа. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |

## Примечания

Граница может быть указана как число, дата и время или специальное «автоматическое» значение.

Экземпляры этого класса неизменяемы.

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
