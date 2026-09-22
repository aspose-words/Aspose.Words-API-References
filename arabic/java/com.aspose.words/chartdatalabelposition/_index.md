---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words لـ Java"
description: "يحدد الموضع لتسمية بيانات المخطط في Java."
type: docs
weight: 74
url: /ar/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

يحدد الموضع لتسمية بيانات المخطط.

 **Remarks:** 

ليس كل أنواع السلاسل تسمح لك بتحديد مواضع التسميات. وتلك التي تسمح بذلك لا تدعم جميع القيم.

 **Examples:** 

يوضح كيفية تعيين موضع تسمية البيانات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ABOVE](#ABOVE) | يحدد أن تسمية البيانات يجب أن تُعرض فوق علامة البيانات. |
| [BELOW](#BELOW) | يحدد أن تسمية البيانات يجب أن تُعرض تحت علامة البيانات. |
| [BEST_FIT](#BEST-FIT) | يحدد أن تسمية البيانات يجب أن تُعرض في أنسب موضع. |
| [CENTER](#CENTER) | يحدد أن يتم عرض تسمية البيانات في مركز علامة البيانات. |
| [INSIDE_BASE](#INSIDE-BASE) | يحدد أن يتم عرض تسمية البيانات داخل قاعدة علامة البيانات. |
| [INSIDE_END](#INSIDE-END) | يحدد أن يتم عرض تسمية البيانات داخل نهاية علامة البيانات. |
| [LEFT](#LEFT) | يحدد أن يتم عرض تسمية البيانات إلى يسار علامة البيانات. |
| [OUTSIDE_END](#OUTSIDE-END) | يحدد أن يتم عرض تسمية البيانات خارج نهاية علامة البيانات. |
| [RIGHT](#RIGHT) | يحدد أن يتم عرض تسمية البيانات إلى يمين علامة البيانات. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


يحدد أن تسمية البيانات يجب أن تُعرض فوق علامة البيانات.

### BELOW {#BELOW}
```
public static int BELOW
```


يحدد أن تسمية البيانات يجب أن تُعرض تحت علامة البيانات.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


يحدد أن تسمية البيانات يجب أن تُعرض في أنسب موضع.

### CENTER {#CENTER}
```
public static int CENTER
```


يحدد أن يتم عرض تسمية البيانات في مركز علامة البيانات.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


يحدد أن يتم عرض تسمية البيانات داخل قاعدة علامة البيانات.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


يحدد أن يتم عرض تسمية البيانات داخل نهاية علامة البيانات.

### LEFT {#LEFT}
```
public static int LEFT
```


يحدد أن يتم عرض تسمية البيانات إلى يسار علامة البيانات.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


يحدد أن يتم عرض تسمية البيانات خارج نهاية علامة البيانات.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


يحدد أن يتم عرض تسمية البيانات إلى يمين علامة البيانات.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
