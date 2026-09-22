---
title: "ChartYValue"
linktitle: "ChartYValue"
second_title: "Aspose.Words لـ Java"
description: "يمثل قيمة Y لسلسلة مخطط في Java."
type: docs
weight: 97
url: /ar/java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

يمثل قيمة Y لسلسلة المخطط.

 **Remarks:** 

تحتوي هذه الفئة على عدد من الطرق الساكنة لإنشاء قيمة Y من نوع معين. تسمح الخاصية [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) لك بتحديد نوع قيمة Y الموجودة.

يجب أن تكون جميع قيم Y غير الفارغة لسلسلة مخطط من نفس النوع [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | يحصل على علم يوضح ما إذا كان الكائن المحدد يساوي كائن قيمة Y الحالي. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | يحصل على قيمة التاريخ والوقت المخزنة. |
| [getDoubleValue()](#getDoubleValue) | يحصل على القيمة الرقمية المخزنة. |
| [getTimeValue()](#getTimeValue) | يحصل على قيمة الوقت المخزنة. |
| [getValueType()](#getValueType) | يحصل على نوع قيمة Y المخزنة في الكائن. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحصل على علم يوضح ما إذا كان الكائن المحدد يساوي كائن قيمة Y الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE).

 **Examples:** 

يعرض كيفية تعبئة سلسلة المخطط بالبيانات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


ينشئ مثيلًا من [ChartYValue](../../com.aspose.words/chartyvalue/) من النوع [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


يحصل على قيمة التاريخ والوقت المخزنة.

**Returns:**
java.util.Date - القيمة المخزنة للوقت والتاريخ.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


يحصل على القيمة الرقمية المخزنة.

**Returns:**
double - القيمة الرقمية المخزنة.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


يحصل على قيمة الوقت المخزنة.

**Returns:**
long - قيمة الوقت المخزنة.
### getValueType() {#getValueType}
```
public int getValueType()
```


يحصل على نوع قيمة Y المخزنة في الكائن.

**Returns:**
int - نوع قيمة Y المخزنة في الكائن. القيمة المرجعة هي واحدة من ثوابت [ChartYValueType](../../com.aspose.words/chartyvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
