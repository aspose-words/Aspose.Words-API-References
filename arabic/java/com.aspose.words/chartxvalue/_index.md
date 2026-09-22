---
title: "ChartXValue"
linktitle: "ChartXValue"
second_title: "Aspose.Words لـ Java"
description: "يمثل قيمة X لسلسلة مخطط في Java."
type: docs
weight: 94
url: /ar/java/com.aspose.words/chartxvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartXValue
```

يمثل قيمة X لسلسلة المخطط.

 **Remarks:** 

تحتوي هذه الفئة على عدد من الطرق الساكنة لإنشاء قيمة X من نوع معين. الخاصية [getValueType()](../../com.aspose.words/chartxvalue/#getValueType) تتيح لك تحديد نوع قيمة X الموجودة.

يجب أن تكون جميع قيم X غير null لسلسلة مخطط من نفس نوع [ChartXValueType](../../com.aspose.words/chartxvaluetype/).

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | يحصل على علم يشير إلى ما إذا كان الكائن المحدد مساويًا لكائن قيمة X الحالي. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.DATE_TIME](../../com.aspose.words/chartxvaluetype/#DATE-TIME). |
| [fromDouble(double value)](#fromDouble-double) | ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/#DOUBLE). |
| [fromMultilevelValue(ChartMultilevelValue value)](#fromMultilevelValue-com.aspose.words.ChartMultilevelValue) | ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/#MULTILEVEL). |
| [fromString(String value)](#fromString-java.lang.String) | ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/#STRING). |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/#TIME). |
| [getDateTimeValue()](#getDateTimeValue) | يحصل على قيمة التاريخ والوقت المخزنة. |
| [getDoubleValue()](#getDoubleValue) | يحصل على القيمة الرقمية المخزنة. |
| [getMultilevelValue()](#getMultilevelValue) | يحصل على القيمة المتعددة المستويات المخزنة. |
| [getStringValue()](#getStringValue) | يحصل على قيمة السلسلة المخزنة. |
| [getTimeValue()](#getTimeValue) | يحصل على قيمة الوقت المخزنة. |
| [getValueType()](#getValueType) | يحصل على نوع قيمة X المخزنة في الكائن. |
| [hashCode()](#hashCode) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحصل على علم يشير إلى ما إذا كان الكائن المحدد مساويًا لكائن قيمة X الحالي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartXValue fromDateTime(Date value)
```


ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.DATE_TIME](../../com.aspose.words/chartxvaluetype/#DATE-TIME).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.Date |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartXValue fromDouble(double value)
```


ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.DOUBLE](../../com.aspose.words/chartxvaluetype/#DOUBLE).

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
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromMultilevelValue(ChartMultilevelValue value) {#fromMultilevelValue-com.aspose.words.ChartMultilevelValue}
```
public static ChartXValue fromMultilevelValue(ChartMultilevelValue value)
```


ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.MULTILEVEL](../../com.aspose.words/chartxvaluetype/#MULTILEVEL).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromString(String value) {#fromString-java.lang.String}
```
public static ChartXValue fromString(String value)
```


ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.STRING](../../com.aspose.words/chartxvaluetype/#STRING).

 **Examples:** 

يعرض كيفية إضافة/إزالة قيم بيانات المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartXValue fromTimeSpan(long value)
```


ينشئ مثيلًا من [ChartXValue](../../com.aspose.words/chartxvalue/) من النوع [ChartXValueType.TIME](../../com.aspose.words/chartxvaluetype/#TIME).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | long |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/)
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
### getMultilevelValue() {#getMultilevelValue}
```
public ChartMultilevelValue getMultilevelValue()
```


يحصل على القيمة المتعددة المستويات المخزنة.

**Returns:**
[ChartMultilevelValue](../../com.aspose.words/chartmultilevelvalue/) - The stored multilevel value.
### getStringValue() {#getStringValue}
```
public String getStringValue()
```


يحصل على قيمة السلسلة المخزنة.

**Returns:**
java.lang.String - قيمة السلسلة المخزنة.
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


يحصل على نوع قيمة X المخزنة في الكائن.

**Returns:**
int - نوع قيمة X المخزنة في الكائن. القيمة المرجعة هي واحدة من ثوابت [ChartXValueType](../../com.aspose.words/chartxvaluetype/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
