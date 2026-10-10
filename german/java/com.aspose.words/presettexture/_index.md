---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words für Java"
description: "Gibt die Textur an, die zum Füllen einer Form in Java verwendet wird."
type: docs
weight: 552
url: /de/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Gibt die Textur an, die zum Füllen einer Form verwendet wird.

 **Examples:** 

Zeigt, wie man das Marker‑Format festlegt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Blaue Tissue-Papier-Textur. |
| [BOUQUET](#BOUQUET) | Blumenstrauß-Textur. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Braune Marmor-Textur. |
| [CANVAS](#CANVAS) | Leinwandtextur. |
| [CORK](#CORK) | Korktextur. |
| [DENIM](#DENIM) | Denim-Textur. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Fischfossil-Textur. |
| [GRANITE](#GRANITE) | Granittextur. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Grüne Marmortextur. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Mittlere Holztextur. |
| [NEWSPRINT](#NEWSPRINT) | Zeitungsdrucktextur. |
| [NONE](#NONE) | Keine Textur. |
| [OAK](#OAK) | Eichentextur. |
| [PAPER_BAG](#PAPER-BAG) | Papierbeutel-Textur. |
| [PAPYRUS](#PAPYRUS) | Papyrustextur. |
| [PARCHMENT](#PARCHMENT) | Pergamenttextur. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Rosa Tissuepapier-Textur. |
| [PURPLE_MESH](#PURPLE-MESH) | Violette Netztextur. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Recycelte Papiertextur. |
| [SAND](#SAND) | Sandtextur. |
| [STATIONERY](#STATIONERY) | Bürobedarf-Textur. |
| [WALNUT](#WALNUT) | Walnuss-Textur. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Wassertropfen-Textur. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Weiße Marmortextur. |
| [WOVEN_MAT](#WOVEN-MAT) | Gewebte Matten-Textur. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Blaue Tissue-Papier-Textur.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Blumenstrauß-Textur.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Braune Marmor-Textur.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Leinwandtextur.

### CORK {#CORK}
```
public static int CORK
```


Korktextur.

### DENIM {#DENIM}
```
public static int DENIM
```


Denim-Textur.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Fischfossil-Textur.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Granittextur.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Grüne Marmortextur.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Mittlere Holztextur.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Zeitungsdrucktextur.

### NONE {#NONE}
```
public static int NONE
```


Keine Textur.

### OAK {#OAK}
```
public static int OAK
```


Eichentextur.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Papierbeutel-Textur.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Papyrustextur.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Pergamenttextur.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Rosa Tissuepapier-Textur.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Violette Netztextur.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Recycelte Papiertextur.

### SAND {#SAND}
```
public static int SAND
```


Sandtextur.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Bürobedarf-Textur.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Walnuss-Textur.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Wassertropfen-Textur.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Weiße Marmortextur.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Gewebte Matten-Textur.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| VoreingestellteTextur | int |  |

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| VoreingestellteTextur | int |  |

**Returns:**
java.lang.String
