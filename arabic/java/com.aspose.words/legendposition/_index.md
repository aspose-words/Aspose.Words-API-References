---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words لـ Java"
description: "يحدد المواقع الممكنة لوسيلة إيضاح المخطط في Java."
type: docs
weight: 420
url: /ar/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

يحدد المواقع الممكنة لوسيلة إيضاح المخطط.

 **Examples:** 

يوضح كيفية تعديل مظهر وسيلة إيضاح المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOTTOM](#BOTTOM) | يحدد أن يتم رسم وسيلة الإيضاح في أسفل المخطط. |
| [LEFT](#LEFT) | يحدد أن يتم رسم وسيلة الإيضاح على يسار المخطط. |
| [NONE](#NONE) | لن يتم عرض وسيلة إيضاح للمخطط. |
| [RIGHT](#RIGHT) | يحدد أن يتم رسم وسيلة الإيضاح على يمين المخطط. |
| [TOP](#TOP) | يحدد أن يتم رسم وسيلة الإيضاح في أعلى المخطط. |
| [TOP_RIGHT](#TOP-RIGHT) | يحدد أن يتم رسم وسيلة الإيضاح في أعلى يمين المخطط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


يحدد أن يتم رسم وسيلة الإيضاح في أسفل المخطط.

### LEFT {#LEFT}
```
public static int LEFT
```


يحدد أن يتم رسم وسيلة الإيضاح على يسار المخطط.

### NONE {#NONE}
```
public static int NONE
```


لن يتم عرض وسيلة إيضاح للمخطط.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


يحدد أن يتم رسم وسيلة الإيضاح على يمين المخطط.

### TOP {#TOP}
```
public static int TOP
```


يحدد أن يتم رسم وسيلة الإيضاح في أعلى المخطط.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


يحدد أن يتم رسم وسيلة الإيضاح في أعلى يمين المخطط.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int legendPosition) {#toString-int}
```
public static String toString(int legendPosition)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
