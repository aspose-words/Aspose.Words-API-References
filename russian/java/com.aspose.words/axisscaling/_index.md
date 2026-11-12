---
title: "AxisScaling"
linktitle: "AxisScaling"
second_title: "Aspose.Words для Java"
description: "Представляет параметры масштабирования оси в Java."
type: docs
weight: 29
url: /ru/java/com.aspose.words/axisscaling/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisScaling implements Cloneable
```

Представляет параметры масштабирования оси.

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Examples:** 

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Методы

| Метод | Описание |
| --- | --- |
| [getLogBase()](#getLogBase) | Возвращает логарифмическую основу для логарифмической оси. |
| [getMaximum()](#getMaximum) | Возвращает максимальное значение оси. |
| [getMinimum()](#getMinimum) | Возвращает минимальное значение оси. |
| [getType()](#getType) | Возвращает тип масштабирования оси. |
| [setLogBase(double value)](#setLogBase-double) | Устанавливает логарифмическую основу для логарифмической оси. |
| [setMaximum(AxisBound value)](#setMaximum-com.aspose.words.AxisBound) | Устанавливает максимальное значение оси. |
| [setMinimum(AxisBound value)](#setMinimum-com.aspose.words.AxisBound) | Устанавливает минимальное значение оси. |
| [setType(int value)](#setType-int) | Устанавливает тип масштабирования оси. |
### getLogBase() {#getLogBase}
```
public double getLogBase()
```


Возвращает логарифмическую основу для логарифмической оси.

 **Remarks:** 

Свойство не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значения с плавающей точкой — от 2 включительно до 1000 включительно. Свойство действует только если [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) установлено в [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

Установка этого свойства задаёт свойство [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) в значение [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

 **Examples:** 

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Returns:**
double — логарифмическая основа для логарифмической оси.
### getMaximum() {#getMaximum}
```
public AxisBound getMaximum()
```


Возвращает максимальное значение оси.

 **Remarks:** 

Значение по умолчанию — "auto".

 **Examples:** 

Показывает, как вставить диаграмму с значениями даты/времени.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
[AxisBound](../../com.aspose.words/axisbound/) - The maximum value of the axis.
### getMinimum() {#getMinimum}
```
public AxisBound getMinimum()
```


Возвращает минимальное значение оси.

 **Remarks:** 

Значение по умолчанию — "auto".

 **Examples:** 

Показывает, как вставить диаграмму с значениями даты/времени.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
[AxisBound](../../com.aspose.words/axisbound/) - Minimum value of the axis.
### getType() {#getType}
```
public int getType()
```


Возвращает тип масштабирования оси.

 **Remarks:** 

Значение [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype/\#LINEAR) — единственное, разрешённое в новых диаграммах MS Office 2016.

 **Examples:** 

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Returns:**
int — тип масштабирования оси. Возвращаемое значение является одной из констант [AxisScaleType](../../com.aspose.words/axisscaletype/).
### setLogBase(double value) {#setLogBase-double}
```
public void setLogBase(double value)
```


Устанавливает логарифмическую основу для логарифмической оси.

 **Remarks:** 

Свойство не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значения с плавающей точкой — от 2 включительно до 1000 включительно. Свойство действует только если [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) установлено в [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

Установка этого свойства задаёт свойство [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) в значение [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

 **Examples:** 

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Логарифмическая основа для логарифмической оси. |

### setMaximum(AxisBound value) {#setMaximum-com.aspose.words.AxisBound}
```
public void setMaximum(AxisBound value)
```


Устанавливает максимальное значение оси.

 **Remarks:** 

Значение по умолчанию — "auto".

 **Examples:** 

Показывает, как вставить диаграмму с значениями даты/времени.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound/) | Максимальное значение оси. |

### setMinimum(AxisBound value) {#setMinimum-com.aspose.words.AxisBound}
```
public void setMinimum(AxisBound value)
```


Устанавливает минимальное значение оси.

 **Remarks:** 

Значение по умолчанию — "auto".

 **Examples:** 

Показывает, как вставить диаграмму с значениями даты/времени.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound/) | Минимальное значение оси. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Устанавливает тип масштабирования оси.

 **Remarks:** 

Значение [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype/\#LINEAR) — единственное, разрешённое в новых диаграммах MS Office 2016.

 **Examples:** 

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Тип масштабирования оси. Значение должно быть одним из констант [AxisScaleType](../../com.aspose.words/axisscaletype/) |

