---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafiğin önceden tanımlı stillerini belirtir."
type: docs
weight: 91
url: /tr/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Bir grafiğin önceden tanımlanmış stillerini belirtir.

 **Examples:** 

Grafik stilini ayarlama ve alma yöntemini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BLACK](#BLACK) | Siyah grafik arka planına sahip bir stil. |
| [BLUE](#BLUE) | Mavi grafik arka planına sahip bir stil. |
| [FLAT](#FLAT) | Gradyansız düz veri noktalarına sahip bir stil. |
| [GRADIENT](#GRADIENT) | Veri noktalarının gradyan dolgulu bir stili. |
| [GREY](#GREY) | Gri gradyan grafik arka planına sahip bir stil. |
| [MUTED](#MUTED) | Susturulmuş renkli bir stil. |
| [NORMAL](#NORMAL) | Varsayılan grafik stilini temsil eder. |
| [ORIGINAL](#ORIGINAL) | Grafiğin özgün görünümüne sahip bir stil. |
| [OUTLINE](#OUTLINE) | Dolgu olmayan, yalnızca bir kenarlık içeren veri noktalarına sahip bir stil. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Siyah grafik arka planına sahip, veri noktalarının dolgu olmadan yalnızca bir kenarlık içerdiği bir stil. |
| [SATURATED](#SATURATED) | Daha doygun renkler içeren bir stil. |
| [SHADED](#SHADED) | Gölgeli veri noktalarına sahip bir stil. |
| [SHADED_PLOT](#SHADED-PLOT) | Çizim alanının gölgeli olduğu bir stil. |
| [SHADOWED](#SHADOWED) | Gölgeye sahip veri noktaları içeren bir stil. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Şeffaf veri noktalarına sahip bir stil. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Şeffaf veri noktalarına sahip bir stil. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Siyah grafik arka planına sahip bir stil.

### BLUE {#BLUE}
```
public static int BLUE
```


Mavi grafik arka planına sahip bir stil.

### FLAT {#FLAT}
```
public static int FLAT
```


Gradyansız düz veri noktalarına sahip bir stil.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Veri noktalarının gradyan dolgulu bir stili.

### GREY {#GREY}
```
public static int GREY
```


Gri gradyan grafik arka planına sahip bir stil.

### MUTED {#MUTED}
```
public static int MUTED
```


Susturulmuş renkli bir stil.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Varsayılan grafik stilini temsil eder.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Grafiğin özgün görünümüne sahip bir stil.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Dolgu olmayan, yalnızca bir kenarlık içeren veri noktalarına sahip bir stil.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Siyah grafik arka planına sahip, veri noktalarının dolgu olmadan yalnızca bir kenarlık içerdiği bir stil.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Daha doygun renkler içeren bir stil.

### SHADED {#SHADED}
```
public static int SHADED
```


Gölgeli veri noktalarına sahip bir stil.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Çizim alanının gölgeli olduğu bir stil.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Gölgeye sahip veri noktaları içeren bir stil.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Şeffaf veri noktalarına sahip bir stil.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Şeffaf veri noktalarına sahip bir stil.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
