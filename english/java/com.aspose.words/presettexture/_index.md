---
title: PresetTexture
linktitle: PresetTexture
second_title: Aspose.Words for Java
description: Specifies texture to be used to fill a shape in Java.
type: docs
weight: 545
url: /java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Specifies texture to be used to fill a shape.

 **Examples:** 

Show how to set marker formatting.

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
## Fields

| Field | Description |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Blue tissue paper texture. |
| [BOUQUET](#BOUQUET) | Bouquet texture. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Brown marble texture. |
| [CANVAS](#CANVAS) | Canvas texture. |
| [CORK](#CORK) | Cork texture. |
| [DENIM](#DENIM) | Denim texture. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Fish fossil texture. |
| [GRANITE](#GRANITE) | Granite texture. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Green marble texture. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Medium wood texture. |
| [NEWSPRINT](#NEWSPRINT) | Newsprint texture. |
| [NONE](#NONE) | No Texture. |
| [OAK](#OAK) | Oak texture. |
| [PAPER_BAG](#PAPER-BAG) | Paper bag texture. |
| [PAPYRUS](#PAPYRUS) | Papyrus texture. |
| [PARCHMENT](#PARCHMENT) | Parchment texture. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Pink tissue paper texture. |
| [PURPLE_MESH](#PURPLE-MESH) | Purple mesh texture. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Recycled paper texture. |
| [SAND](#SAND) | Sand texture. |
| [STATIONERY](#STATIONERY) | Stationery texture. |
| [WALNUT](#WALNUT) | Walnut texture. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Water droplets texture. |
| [WHITE_MARBLE](#WHITE-MARBLE) | White marble texture. |
| [WOVEN_MAT](#WOVEN-MAT) | Woven mat texture. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Blue tissue paper texture.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Bouquet texture.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Brown marble texture.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Canvas texture.

### CORK {#CORK}
```
public static int CORK
```


Cork texture.

### DENIM {#DENIM}
```
public static int DENIM
```


Denim texture.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Fish fossil texture.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Granite texture.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Green marble texture.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Medium wood texture.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Newsprint texture.

### NONE {#NONE}
```
public static int NONE
```


No Texture.

### OAK {#OAK}
```
public static int OAK
```


Oak texture.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Paper bag texture.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Papyrus texture.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Parchment texture.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Pink tissue paper texture.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Purple mesh texture.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Recycled paper texture.

### SAND {#SAND}
```
public static int SAND
```


Sand texture.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Stationery texture.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Walnut texture.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Water droplets texture.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


White marble texture.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Woven mat texture.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
