---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию размеров пузырей для серии диаграммы в Java."
type: docs
weight: 50
url: /ru/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Представляет коллекцию размеров пузырей для серии диаграммы.

 **Remarks:** 

Коллекция позволяет только изменять размеры пузырей. Чтобы добавить или вставить новые значения в серию диаграммы, либо удалить значения, можно использовать соответствующие методы класса [ChartSeries](../../com.aspose.words/chartseries/).

Пустые значения размеров пузырей представлены как double\#NA\_N.NA\_N.
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Возвращает значение размера пузыря по указанному индексу. |
| [getCount()](#getCount) | Получает количество элементов в этой коллекции. |
| [getFormatCode()](#getFormatCode) | Возвращает код формата, применяемый к размерам пузырей. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
| [set(int index, double value)](#set-int-double) | Устанавливает значение размера пузыря по указанному индексу. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Устанавливает код формата, применяемый к размерам пузырей. |
### get(int index) {#get-int}
```
public double get(int index)
```


Возвращает значение размера пузыря по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
double - Значение размера пузыря по указанному индексу.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов в этой коллекции.

**Returns:**
int - количество элементов в этой коллекции.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Возвращает код формата, применяемый к размерам пузырей.

 **Remarks:** 

Форматирование чисел используется для изменения отображения значений в диаграмме. Примеры форматов чисел:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Дробь - "\# ?/?"

Научный - "0.00E+00"

Бухгалтерский - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Пользовательский с цветом - "[Red]-\#,\#\#0.0"

 **Examples:** 

Показывает, как работать с кодом формата данных диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
java.lang.String - Код формата, применяемый к размерам пузырей.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Устанавливает значение размера пузыря по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |
| значение | double | Значение размера пузыря по указанному индексу. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Устанавливает код формата, применяемый к размерам пузырей.

 **Remarks:** 

Форматирование чисел используется для изменения отображения значений в диаграмме. Примеры форматов чисел:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Дробь - "\# ?/?"

Научный - "0.00E+00"

Бухгалтерский - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Пользовательский с цветом - "[Red]-\#,\#\#0.0"

 **Examples:** 

Показывает, как работать с кодом формата данных диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Код формата, применяемый к размерам пузырей. |

