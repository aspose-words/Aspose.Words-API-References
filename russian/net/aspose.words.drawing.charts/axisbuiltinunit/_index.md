---
title: AxisBuiltInUnit Enum
linktitle: AxisBuiltInUnit
articleTitle: AxisBuiltInUnit
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.Charts.AxisBuiltInUnit для настраиваемых единиц отображения осей, повышающих ясность и эффективность вашей диаграммы.
type: docs
weight: 760
url: /ru/net/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enumeration

Указывает единицы отображения для оси.

```csharp
public enum AxisBuiltInUnit
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Указывает, что значения на диаграмме должны отображаться как есть. |
| Custom | `1` | Указывает, что значения на диаграмме должны быть разделены на определяемый пользователем делитель. Это значение не поддерживается новыми типами диаграмм MS Office 2016. |
| Billions | `2` | Указывает, что значения на диаграмме должны быть разделены на 1 000 000 000. |
| HundredMillions | `3` | Указывает, что значения на диаграмме должны быть разделены на 100 000 000. |
| Hundreds | `4` | Указывает, что значения на диаграмме должны быть разделены на 100. |
| HundredThousands | `5` | Указывает, что значения на диаграмме должны быть разделены на 100 000. |
| Millions | `6` | Указывает, что значения на диаграмме должны быть разделены на 1 000 000. |
| TenMillions | `7` | Указывает, что значения на диаграмме должны быть разделены на 10 000 000. |
| TenThousands | `8` | Указывает, что значения на диаграмме должны быть разделены на 10 000. |
| Thousands | `9` | Указывает, что значения на диаграмме должны быть разделены на 1000. |
| Trillions | `10` | Указывает, что значения на диаграмме должны быть разделены на 1,000,000,000,0000. |
| Percentage | `11` | Указывает, что значения на диаграмме должны быть разделены на 0,01. Это значение поддерживается только новыми типами chart MS Office 2016. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
