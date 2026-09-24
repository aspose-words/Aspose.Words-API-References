---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekli doldurmak için kullanılacak dokuyu belirtir."
type: docs
weight: 552
url: /tr/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Bir şekli doldurmak için kullanılacak dokuyu belirtir.

 **Examples:** 

İşaretleyici biçimlendirmesinin nasıl ayarlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Mavi kağıt havlu dokusu. |
| [BOUQUET](#BOUQUET) | Buklet dokusu. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Kahverengi mermer dokusu. |
| [CANVAS](#CANVAS) | Kanvas dokusu. |
| [CORK](#CORK) | Mantar dokusu. |
| [DENIM](#DENIM) | Kot dokusu. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Balık fosili dokusu. |
| [GRANITE](#GRANITE) | Granit dokusu. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Yeşil mermer dokusu. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Orta ahşap dokusu. |
| [NEWSPRINT](#NEWSPRINT) | Gazete kağıdı dokusu. |
| [NONE](#NONE) | Doku Yok. |
| [OAK](#OAK) | Meşe dokusu. |
| [PAPER_BAG](#PAPER-BAG) | Kağıt torba dokusu. |
| [PAPYRUS](#PAPYRUS) | Papirüs dokusu. |
| [PARCHMENT](#PARCHMENT) | Parşömen dokusu. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Pembe peçete kağıdı dokusu. |
| [PURPLE_MESH](#PURPLE-MESH) | Mor ağ dokusu. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Geri dönüştürülmüş kağıt dokusu. |
| [SAND](#SAND) | Kum dokusu. |
| [STATIONERY](#STATIONERY) | Kırtasiye dokusu. |
| [WALNUT](#WALNUT) | Ceviz dokusu. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Su damlaları dokusu. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Beyaz mermer dokusu. |
| [WOVEN_MAT](#WOVEN-MAT) | Örgülü paspas dokusu. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Mavi kağıt havlu dokusu.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Buklet dokusu.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Kahverengi mermer dokusu.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Kanvas dokusu.

### CORK {#CORK}
```
public static int CORK
```


Mantar dokusu.

### DENIM {#DENIM}
```
public static int DENIM
```


Kot dokusu.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Balık fosili dokusu.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Granit dokusu.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Yeşil mermer dokusu.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Orta ahşap dokusu.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Gazete kağıdı dokusu.

### NONE {#NONE}
```
public static int NONE
```


Doku Yok.

### OAK {#OAK}
```
public static int OAK
```


Meşe dokusu.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Kağıt torba dokusu.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Papirüs dokusu.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Parşömen dokusu.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Pembe peçete kağıdı dokusu.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Mor ağ dokusu.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Geri dönüştürülmüş kağıt dokusu.

### SAND {#SAND}
```
public static int SAND
```


Kum dokusu.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Kırtasiye dokusu.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Ceviz dokusu.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Su damlaları dokusu.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Beyaz mermer dokusu.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Örgülü paspas dokusu.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
