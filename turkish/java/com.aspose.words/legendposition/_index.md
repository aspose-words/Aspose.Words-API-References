---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik açıklamasının olası konumlarını belirtir."
type: docs
weight: 420
url: /tr/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Bir grafik açıklaması için olası konumları belirtir.

 **Examples:** 

Grafiğin açıklamasının görünümünü nasıl düzenleyeceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTTOM](#BOTTOM) | Açıklamanın grafiğin altında çizileceğini belirtir. |
| [LEFT](#LEFT) | Açıklamanın grafiğin solunda çizileceğini belirtir. |
| [NONE](#NONE) | Grafik için açıklama gösterilmeyecek. |
| [RIGHT](#RIGHT) | Açıklamanın grafiğin sağında çizileceğini belirtir. |
| [TOP](#TOP) | Açıklamanın grafiğin üstünde çizileceğini belirtir. |
| [TOP_RIGHT](#TOP-RIGHT) | Açıklamanın grafiğin sağ üst köşesinde çizileceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Açıklamanın grafiğin altında çizileceğini belirtir.

### LEFT {#LEFT}
```
public static int LEFT
```


Açıklamanın grafiğin solunda çizileceğini belirtir.

### NONE {#NONE}
```
public static int NONE
```


Grafik için açıklama gösterilmeyecek.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Açıklamanın grafiğin sağında çizileceğini belirtir.

### TOP {#TOP}
```
public static int TOP
```


Açıklamanın grafiğin üstünde çizileceğini belirtir.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Açıklamanın grafiğin sağ üst köşesinde çizileceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
