---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words для Java"
description: "Представляет значение X для серии диаграммы в Java."
type: docs
weight: 94
url: /ru/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

Представляет значение X для серии диаграммы.

 **Remarks:** 

Этот класс содержит несколько статических методов для создания значения X определённого типа. Свойство [getValueType()](../../com.aspose.words/chartxvalue/\#getValueType) позволяет определить тип существующего значения X.

Все ненулевые значения X серии диаграммы должны быть одного типа [ChartXValueType](../../com.aspose.words/chartxvaluetype/).

 **Examples:** 

Показывает, как заполнить серию диаграммы данными.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения X. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Возвращает сохранённое значение даты и времени. |
| [getDoubleValue()](#getDoubleValue) | Возвращает сохранённое числовое значение. |
| [getMultilevelValue()](#getMultilevelValue) | Возвращает сохранённое многоуровневое значение. |
| [getStringValue()](#getStringValue) | Получает сохранённое строковое значение. |
| [getTimeValue()](#getTimeValue) | Получает сохранённое значение времени. |
| [getValueType()](#getValueType) | Получает тип значения X, сохранённого в объекте. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения X.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.DATE\_TIME](../../com.aspose.words/chartxvaluetype/\#DATE-TIME).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/\#DOUBLE).

 **Examples:** 

Показывает, как заполнить серию диаграммы данными.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/\#MULTILEVEL).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/\#STRING).

 **Examples:** 

Показывает, как добавлять/удалять значения данных диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


Создаёт экземпляр [ChartXValue](../../com.aspose.words/chartxvalue/) типа [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/\#TIME).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Возвращает сохранённое значение даты и времени.

**Returns:**
java.util.Date — Сохранённое значение даты и времени.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Возвращает сохранённое числовое значение.

**Returns:**
double — Сохранённое числовое значение.
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


Возвращает сохранённое многоуровневое значение.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


Получает сохранённое строковое значение.

**Returns:**
java.lang.String — Сохранённое строковое значение.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Получает сохранённое значение времени.

**Returns:**
long — Сохранённое значение времени.
### getValueType() {#getValueType}
```
public int getValueType()
```


Получает тип значения X, сохранённого в объекте.

**Returns:**
int — Тип значения X, сохранённого в объекте. Возвращаемое значение является одной из констант [ChartXValueType](../../com.aspose.words/chartxvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
