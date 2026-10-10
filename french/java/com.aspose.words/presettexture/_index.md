---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words pour Java"
description: "Spécifie la texture à utiliser pour remplir une forme en Java."
type: docs
weight: 552
url: /fr/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Spécifie la texture à utiliser pour remplir une forme.

 **Examples:** 

Montre comment définir le format du marqueur.

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
## Champs

| Champ | Description |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Texture de papier de soie bleu. |
| [BOUQUET](#BOUQUET) | Texture de bouquet. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Texture de marbre brun. |
| [CANVAS](#CANVAS) | Texture de toile. |
| [CORK](#CORK) | Texture de liège. |
| [DENIM](#DENIM) | Texture de denim. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Texture de fossile de poisson. |
| [GRANITE](#GRANITE) | Texture de granit. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Texture de marbre vert. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Texture de bois moyen. |
| [NEWSPRINT](#NEWSPRINT) | Texture de papier journal. |
| [NONE](#NONE) | Pas de texture. |
| [OAK](#OAK) | Texture de chêne. |
| [PAPER_BAG](#PAPER-BAG) | Texture de sac en papier. |
| [PAPYRUS](#PAPYRUS) | Texture de papyrus. |
| [PARCHMENT](#PARCHMENT) | Texture de parchemin. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Texture de papier de soie rose. |
| [PURPLE_MESH](#PURPLE-MESH) | Texture de maille violette. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Texture de papier recyclé. |
| [SAND](#SAND) | Texture de sable. |
| [STATIONERY](#STATIONERY) | Texture de papeterie. |
| [WALNUT](#WALNUT) | Texture de noyer. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Texture de gouttelettes d'eau. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Texture de marbre blanc. |
| [WOVEN_MAT](#WOVEN-MAT) | Texture de tapis tissé. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Texture de papier de soie bleu.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Texture de bouquet.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Texture de marbre brun.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Texture de toile.

### CORK {#CORK}
```
public static int CORK
```


Texture de liège.

### DENIM {#DENIM}
```
public static int DENIM
```


Texture de denim.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Texture de fossile de poisson.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Texture de granit.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Texture de marbre vert.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Texture de bois moyen.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Texture de papier journal.

### NONE {#NONE}
```
public static int NONE
```


Pas de texture.

### OAK {#OAK}
```
public static int OAK
```


Texture de chêne.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Texture de sac en papier.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Texture de papyrus.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Texture de parchemin.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Texture de papier de soie rose.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Texture de maille violette.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Texture de papier recyclé.

### SAND {#SAND}
```
public static int SAND
```


Texture de sable.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Texture de papeterie.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Texture de noyer.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Texture de gouttelettes d'eau.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Texture de marbre blanc.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Texture de tapis tissé.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
