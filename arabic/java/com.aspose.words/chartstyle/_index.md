---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words لـ Java"
description: "يحدد الأنماط المعرّفة مسبقًا لمخطط في Java."
type: docs
weight: 91
url: /ar/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

يحدد الأنماط المحددة مسبقًا للمخطط.

 **Examples:** 

يوضح كيفية تعيين واسترجاع نمط المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart in the Black style.
 builder.insertChart(ChartType.COLUMN, 400.0, 250.0, ChartStyle.BLACK);

 doc.save(getArtifactsDir() + "Charts.SetChartStyle.docx");

 doc = new Document(getArtifactsDir() + "Charts.SetChartStyle.docx");

 // Get a chart to update.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();

 // Get the chart style.
 Assert.assertEquals(ChartStyle.BLACK, chart.getStyle());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BLACK](#BLACK) | نمط بخلفية مخطط سوداء. |
| [BLUE](#BLUE) | نمط بخلفية مخطط زرقاء. |
| [FLAT](#FLAT) | نمط بنقاط بيانات مسطحة بدون تدرج. |
| [GRADIENT](#GRADIENT) | نمط بملء تدرجي لنقاط البيانات. |
| [GREY](#GREY) | نمط بخلفية مخطط تدرج رمادي. |
| [MUTED](#MUTED) | نمط بألوان خافتة. |
| [NORMAL](#NORMAL) | يمثل النمط الافتراضي للمخطط. |
| [ORIGINAL](#ORIGINAL) | نمط بمظهر أصلي للمخطط. |
| [OUTLINE](#OUTLINE) | نمط يحتوي على نقاط بيانات بدون تعبئة، بل فقط حدود. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | نمط بخلفية مخطط سوداء، حيث لا تحتوي نقاط البيانات على تعبئة، بل فقط حدود. |
| [SATURATED](#SATURATED) | نمط بألوان أكثر تشبعًا. |
| [SHADED](#SHADED) | نمط بنقاط بيانات مظللة. |
| [SHADED_PLOT](#SHADED-PLOT) | نمط، حيث تكون منطقة الرسم مظللة. |
| [SHADOWED](#SHADOWED) | نمط بنقاط بيانات ذات ظل. |
| [TRANSPARENT_1](#TRANSPARENT-1) | نمط بنقاط بيانات شفافة. |
| [TRANSPARENT_2](#TRANSPARENT-2) | نمط بنقاط بيانات شفافة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


نمط بخلفية مخطط سوداء.

### BLUE {#BLUE}
```
public static int BLUE
```


نمط بخلفية مخطط زرقاء.

### FLAT {#FLAT}
```
public static int FLAT
```


نمط بنقاط بيانات مسطحة بدون تدرج.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


نمط بملء تدرجي لنقاط البيانات.

### GREY {#GREY}
```
public static int GREY
```


نمط بخلفية مخطط تدرج رمادي.

### MUTED {#MUTED}
```
public static int MUTED
```


نمط بألوان خافتة.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


يمثل النمط الافتراضي للمخطط.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


نمط بمظهر أصلي للمخطط.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


نمط يحتوي على نقاط بيانات بدون تعبئة، بل فقط حدود.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


نمط بخلفية مخطط سوداء، حيث لا تحتوي نقاط البيانات على تعبئة، بل فقط حدود.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


نمط بألوان أكثر تشبعًا.

### SHADED {#SHADED}
```
public static int SHADED
```


نمط بنقاط بيانات مظللة.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


نمط، حيث تكون منطقة الرسم مظللة.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


نمط بنقاط بيانات ذات ظل.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


نمط بنقاط بيانات شفافة.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


نمط بنقاط بيانات شفافة.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartStyle) {#toString-int}
```
public static String toString(int chartStyle)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
