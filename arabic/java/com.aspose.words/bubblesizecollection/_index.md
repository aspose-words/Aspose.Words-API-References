---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من أحجام الفقاعات لسلسلة مخطط في Java."
type: docs
weight: 50
url: /ar/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

يمثل مجموعة من أحجام الفقاعات لسلسلة مخطط.

 **Remarks:** 

تسمح المجموعة فقط بتغيير أحجام الفقاعات. لإضافة أو إدراج قيم جديدة إلى سلسلة مخطط، أو لإزالة القيم، يمكن استخدام الأساليب المناسبة من الفئة [ChartSeries](../../com.aspose.words/chartseries/).

يتم تمثيل قيم أحجام الفقاعات الفارغة كـ double\#NA\_N.NA\_N.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int index)](#get-int) | يحصل على قيمة حجم الفقاعة في الفهرس المحدد. |
| [getCount()](#getCount) | يحصل على عدد العناصر في هذه المجموعة. |
| [getFormatCode()](#getFormatCode) | يحصل على رمز التنسيق المطبق على أحجام الفقاعات. |
| [iterator()](#iterator) | يرجع كائن عداد. |
| [set(int index, double value)](#set-int-double) | يضبط قيمة حجم الفقاعة في الفهرس المحدد. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | يضبط رمز التنسيق المطبق على أحجام الفقاعات. |
### get(int index) {#get-int}
```
public double get(int index)
```


يحصل على قيمة حجم الفقاعة في الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
double - قيمة حجم الفقاعة في الفهرس المحدد.
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


يحصل على رمز التنسيق المطبق على أحجام الفقاعات.

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
java.lang.String - رمز التنسيق المطبق على أحجام الفقاعات.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


يضبط قيمة حجم الفقاعة في الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |
| قيمة | double | قيمة حجم الفقاعة في الفهرس المحدد. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


يضبط رمز التنسيق المطبق على أحجام الفقاعات.

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
| قيمة | java.lang.String | رمز التنسيق المطبق على أحجام الفقاعات. |

