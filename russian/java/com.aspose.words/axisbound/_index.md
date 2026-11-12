---
title: "AxisBound"
linktitle: "AxisBound"
second_title: "Aspose.Words для Java"
description: "Представляет минимальную или максимальную границу значений оси в Java."
type: docs
weight: 22
url: /ru/java/com.aspose.words/axisbound/
---

**Inheritance:**
java.lang.Object
```
public class AxisBound
```

Представляет минимальную или максимальную границу значений оси.

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Remarks:** 

Граница может быть указана как числовое, datetime или специальное значение "auto".

Экземпляры этого класса неизменяемы.

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [AxisBound()](#AxisBound) | Создаёт новый экземпляр, указывающий, что граница оси должна определяться автоматически приложением для обработки текста. |
| [AxisBound(double value)](#AxisBound-double) | Создаёт границу оси, представленную числом. |
| [AxisBound(Date datetime)](#AxisBound-java.util.Date) | Создаёт границу оси, представленную значением datetime. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getValue()](#getValue) | Возвращает числовое значение границы оси. |
| [getValueAsDate()](#getValueAsDate) | Возвращает значение границы оси, представленное как дата и время. |
| [hashCode()](#hashCode) |  |
| [isAuto()](#isAuto) | Возвращает флаг, указывающий, что граница оси должна определяться автоматически. |
| [toString()](#toString) | Возвращает удобочитаемую строку, отображающую значение этого объекта. |
### AxisBound() {#AxisBound}
```
public AxisBound()
```


Создаёт новый экземпляр, указывающий, что граница оси должна определяться автоматически приложением для обработки текста.

 **Examples:** 

Показывает, как установить пользовательские границы оси.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

### AxisBound(double value) {#AxisBound-double}
```
public AxisBound(double value)
```


Создаёт границу оси, представленную числом.

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
| значение | double |  |

### AxisBound(Date datetime) {#AxisBound-java.util.Date}
```
public AxisBound(Date datetime)
```


Создаёт границу оси, представленную значением datetime.

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
| datetime | java.util.Date |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getValue() {#getValue}
```
public double getValue()
```


Возвращает числовое значение границы оси.

 **Examples:** 

Показывает, как установить пользовательские границы оси.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
double - Числовое значение границы оси.
### getValueAsDate() {#getValueAsDate}
```
public Date getValueAsDate()
```


Возвращает значение границы оси, представленное как дата и время.

 **Examples:** 

Показывает, как установить пользовательские границы оси.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
java.util.Date - Значение границы оси, представленное как datetime.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isAuto() {#isAuto}
```
public boolean isAuto()
```


Возвращает флаг, указывающий, что граница оси должна определяться автоматически.

 **Examples:** 

Показывает, как установить пользовательские границы оси.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
boolean - Флаг, указывающий, что граница оси должна определяться автоматически.
### toString() {#toString}
```
public String toString()
```


Возвращает удобочитаемую строку, отображающую значение этого объекта.

**Returns:**
java.lang.String
