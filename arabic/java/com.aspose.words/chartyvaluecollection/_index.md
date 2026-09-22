---
title: "ChartYValueCollection"
linktitle: "ChartYValueCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من قيم Y لسلسلة مخطط في Java."
type: docs
weight: 98
url: /ar/java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

يمثل مجموعة من قيم Y لسلسلة المخطط.

 **Remarks:** 

جميع عناصر المجموعة باستثناء **null** يجب أن تكون لها نفس [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\#getValueType).

المجموعة تسمح فقط بتغيير قيم Y. لإضافة أو إدراج قيم جديدة إلى سلسلة مخطط، أو إزالة القيم، يمكن استخدام الأساليب المناسبة من الفئة [ChartSeries](../../com.aspose.words/chartseries/).

 **Examples:** 

يظهر كيفية الحصول على بيانات سلسلة المخطط.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يحصل على قيمة Y في الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد العناصر في هذه المجموعة. |
| [getFormatCode()](#getFormatCode) | يحصل على رمز التنسيق المطبق على قيم Y. |
| [iterator()](#iterator) | يرجع كائن عداد. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | يضبط قيمة Y في الفهرس المحدد. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | يضبط رمز التنسيق المطبق على قيم Y. |
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


يحصل على قيمة Y في الفهرس المحدد.

 **Remarks:** 

القيم الفارغة تمثل كـ **null**.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد العناصر في هذه المجموعة.

**Returns:**
int - عدد العناصر في هذه المجموعة.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


يحصل على رمز التنسيق المطبق على قيم Y.

 **Remarks:** 

يُستخدم تنسيق الأرقام لتغيير طريقة ظهور القيم في المخطط. أمثلة تنسيقات الأرقام:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

كسر - "\# ?/?"

علمي - "0.00E+00"

محاسبة - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

مخصص مع اللون - "[Red]-\#,\#\#0.0"

 **Examples:** 

يعرض كيفية التعامل مع رمز التنسيق لبيانات المخطط.

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
java.lang.String - رمز التنسيق المطبق على قيم Y.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

**Returns:**
java.util.Iterator
### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


يضبط قيمة Y في الفهرس المحدد.

 **Remarks:** 

القيم الفارغة تمثل كـ **null**.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | قيمة Y عند الفهرس المحدد. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


يضبط رمز التنسيق المطبق على قيم Y.

 **Remarks:** 

يُستخدم تنسيق الأرقام لتغيير طريقة ظهور القيم في المخطط. أمثلة تنسيقات الأرقام:

Number - "\#,\#\#0.00"

Currency - "\\"$\\"\#,\#\#0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

كسر - "\# ?/?"

علمي - "0.00E+00"

محاسبة - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

مخصص مع اللون - "[Red]-\#,\#\#0.0"

 **Examples:** 

يعرض كيفية التعامل مع رمز التنسيق لبيانات المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | رمز التنسيق المطبق على قيم Y. |

