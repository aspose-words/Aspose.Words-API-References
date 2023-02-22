---
title: Enum AxisBuiltInUnit
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.AxisBuiltInUnit перечисление. Определяет единицы отображения для оси.
type: docs
weight: 510
url: /ru/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Определяет единицы отображения для оси.

```csharp
public enum AxisBuiltInUnit
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Указывает, что значения на диаграмме должны отображаться как есть. |
| Custom | `1` | Указывает, что значения на диаграмме должны быть разделены на заданный пользователем делитель. Это значение не поддерживается новыми типами диаграмм MS Office 2016. |
| Billions | `2` | Указывает, что значения на диаграмме должны быть разделены на 1 000 000 000. |
| HundredMillions | `3` | Указывает, что значения на диаграмме должны быть разделены на 100 000 000. |
| Hundreds | `4` | Указывает, что значения на диаграмме должны быть разделены на 100. |
| HundredThousands | `5` | Указывает, что значения на диаграмме должны быть разделены на 100 000. |
| Millions | `6` | Указывает, что значения на диаграмме должны быть разделены на 1 000 000. |
| TenMillions | `7` | Указывает, что значения на диаграмме должны быть разделены на 10 000 000. |
| TenThousands | `8` | Указывает, что значения на диаграмме должны быть разделены на 10 000. |
| Thousands | `9` | Указывает, что значения на диаграмме должны быть разделены на 1000. |
| Trillions | `10` | Указывает, что значения на диаграмме должны быть разделены на 1 000 000 000 0000. |
| Percentage | `11` | Указывает, что значения на диаграмме должны быть разделены на 0,01. Это значение поддерживается только новыми типами chart MS Office 2016. |

### Примеры

Показывает, как управлять делениями и отображаемыми значениями оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Установите второстепенные деления оси Y так, чтобы они указывали в сторону от области графика,
// и основные деления для пересечения оси.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Установите ось Y, чтобы показать основной тик каждые 10 единиц и второстепенный тик каждые 1 единицу.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Установите границы оси Y на -10 и 20.
// Эта ось Y теперь будет отображать 4 основных деления и 27 второстепенных делений.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Для оси X установите основные деления через каждые 10 единиц,
// каждая второстепенная отметка на 2,5 единицы.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Настройте оба типа делений, чтобы они отображались внутри области построения графика.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Установите границы по оси X так, чтобы ось X охватывала 5 основных делений и 12 второстепенных делений.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Установите метки тиков, чтобы отображать их значение в миллионах.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Мы можем установить более конкретное значение, по которому метки тиков будут отображать свои значения.
// Этот оператор эквивалентен приведенному выше.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


