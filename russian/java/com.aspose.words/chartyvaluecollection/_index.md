---
title: "ChartYValueCollection"
linktitle: "ChartYValueCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию значений Y для серии диаграммы в Java."
type: docs
weight: 98
url: /ru/java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

Представляет коллекцию значений Y для серии диаграммы.

 **Remarks:** 

Все элементы коллекции, кроме **null**, должны иметь одинаковый тип, возвращаемый [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\#getValueType).

Коллекция позволяет только изменять значения Y. Чтобы добавить или вставить новые значения в серию диаграммы, либо удалить значения, можно использовать соответствующие методы класса [ChartSeries](../../com.aspose.words/chartseries/).

 **Examples:** 

Показывает, как получить данные серии диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series = chart.getSeries().get(0);

 double minValue = Double.MAX_VALUE;
 int minValueIndex = 0;
 double maxValue = -Double.MAX_VALUE;
 int maxValueIndex = 0;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     // Clear individual format of all data points.
     // Data points and data values are one-to-one in column charts.
     series.getDataPoints().get(i).clearFormat();

     // Get Y value.
     double yValue = series.getYValues().get(i).getDoubleValue();

     if (yValue < minValue)
     {
         minValue = yValue;
         minValueIndex = i;
     }

     if (yValue > maxValue)
     {
         maxValue = yValue;
         maxValueIndex = i;
     }
 }

 // Change colors of the max and min values.
 series.getDataPoints().get(minValueIndex).getFormat().getFill().setForeColor(Color.RED);
 series.getDataPoints().get(maxValueIndex).getFormat().getFill().setForeColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Charts.GetChartSeriesData.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Получает значение Y по указанному индексу. |
| [getCount()](#getCount) | Получает количество элементов в этой коллекции. |
| [getFormatCode()](#getFormatCode) | Получает код формата, применённый к значениям Y. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Устанавливает значение Y по указанному индексу. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Устанавливает код формата, применённый к значениям Y. |
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


Получает значение Y по указанному индексу.

 **Remarks:** 

Пустые значения представлены как **null**.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
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


Получает код формата, применённый к значениям Y.

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
java.lang.String - Код формата, применяемый к значениям Y.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


Устанавливает значение Y по указанному индексу.

 **Remarks:** 

Пустые значения представлены как **null**.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | Значение Y по указанному индексу. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Устанавливает код формата, применённый к значениям Y.

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
| значение | java.lang.String | Код формата, применяемый к значениям Y. |

