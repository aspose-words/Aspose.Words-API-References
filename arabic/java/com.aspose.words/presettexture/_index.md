---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words لـ Java"
description: "يحدد النسيج المستخدم لملء الشكل في Java."
type: docs
weight: 552
url: /ar/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

يحدد النسيج الذي سيُستخدم لملء الشكل.

 **Examples:** 

يعرض كيفية تعيين تنسيق العلامة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | نسيج ورق مناديل أزرق. |
| [BOUQUET](#BOUQUET) | نسيج باقة. |
| [BROWN_MARBLE](#BROWN-MARBLE) | نسيج رخام بني. |
| [CANVAS](#CANVAS) | ملمس القماش. |
| [CORK](#CORK) | ملمس الفلين. |
| [DENIM](#DENIM) | ملمس الدنيم. |
| [FISH_FOSSIL](#FISH-FOSSIL) | ملمس أحفورة السمك. |
| [GRANITE](#GRANITE) | ملمس الجرانيت. |
| [GREEN_MARBLE](#GREEN-MARBLE) | ملمس الرخام الأخضر. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | ملمس الخشب المتوسط. |
| [NEWSPRINT](#NEWSPRINT) | ملمس ورق الصحف. |
| [NONE](#NONE) | بدون ملمس. |
| [OAK](#OAK) | ملمس البلوط. |
| [PAPER_BAG](#PAPER-BAG) | ملمس حقيبة الورق. |
| [PAPYRUS](#PAPYRUS) | ملمس البردي. |
| [PARCHMENT](#PARCHMENT) | ملمس الرق. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | ملمس ورق المناديل الوردي. |
| [PURPLE_MESH](#PURPLE-MESH) | ملمس الشبكة البنفسجية. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | ملمس الورق المعاد تدويره. |
| [SAND](#SAND) | ملمس الرمل. |
| [STATIONERY](#STATIONERY) | ملمس الأدوات المكتبية. |
| [WALNUT](#WALNUT) | ملمس الجوز. |
| [WATER_DROPLETS](#WATER-DROPLETS) | ملمس قطرات الماء. |
| [WHITE_MARBLE](#WHITE-MARBLE) | ملمس الرخام الأبيض. |
| [WOVEN_MAT](#WOVEN-MAT) | ملمس الحصيرة المنسوجة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


نسيج ورق مناديل أزرق.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


نسيج باقة.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


نسيج رخام بني.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


ملمس القماش.

### CORK {#CORK}
```
public static int CORK
```


ملمس الفلين.

### DENIM {#DENIM}
```
public static int DENIM
```


ملمس الدنيم.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


ملمس أحفورة السمك.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


ملمس الجرانيت.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


ملمس الرخام الأخضر.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


ملمس الخشب المتوسط.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


ملمس ورق الصحف.

### NONE {#NONE}
```
public static int NONE
```


بدون ملمس.

### OAK {#OAK}
```
public static int OAK
```


ملمس البلوط.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


ملمس حقيبة الورق.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


ملمس البردي.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


ملمس الرق.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


ملمس ورق المناديل الوردي.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


ملمس الشبكة البنفسجية.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


ملمس الورق المعاد تدويره.

### SAND {#SAND}
```
public static int SAND
```


ملمس الرمل.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


ملمس الأدوات المكتبية.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


ملمس الجوز.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


ملمس قطرات الماء.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


ملمس الرخام الأبيض.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


ملمس الحصيرة المنسوجة.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int presetTexture) {#toString-int}
```
public static String toString(int presetTexture)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
