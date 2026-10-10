---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words для Java"
description: "Представляет значение Y для серии диаграммы в Java."
type: docs
weight: 97
url: /ru/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Представляет значение Y для серии диаграммы.

 **Remarks:** 

Этот класс содержит несколько статических методов для создания значения Y определённого типа. Свойство [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) позволяет определить тип существующего значения Y.

Все ненулевые значения Y серии диаграммы должны быть одного типа [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения Y. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | Возвращает сохранённое значение даты и времени. |
| [getDoubleValue()](#getDoubleValue) | Возвращает сохранённое числовое значение. |
| [getTimeValue()](#getTimeValue) | Получает сохранённое значение времени. |
| [getValueType()](#getValueType) | Возвращает тип значения Y, хранящегося в объекте. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Возвращает флаг, указывающий, равен ли указанный объект текущему объекту значения Y.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

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
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Создаёт экземпляр [ChartYValue](../../com.aspose.words/chartyvalue/) типа [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
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


Возвращает тип значения Y, хранящегося в объекте.

**Returns:**
int — тип значения Y, хранящегося в объекте. Возвращаемое значение является одной из констант [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
