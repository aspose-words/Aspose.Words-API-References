---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words per Java"
description: "Specifica la texture da utilizzare per riempire una forma in Java."
type: docs
weight: 552
url: /it/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Specifica la trama da utilizzare per riempire una forma.

 **Examples:** 

Mostra come impostare la formattazione del marcatore.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Texture di carta velina blu. |
| [BOUQUET](#BOUQUET) | Texture a bouquet. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Texture di marmo marrone. |
| [CANVAS](#CANVAS) | Texture di tela. |
| [CORK](#CORK) | Texture di sughero. |
| [DENIM](#DENIM) | Texture di denim. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Texture di fossile di pesce. |
| [GRANITE](#GRANITE) | Texture di granito. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Texture di marmo verde. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Texture di legno medio. |
| [NEWSPRINT](#NEWSPRINT) | Texture di carta da giornale. |
| [NONE](#NONE) | Nessuna texture. |
| [OAK](#OAK) | Texture di quercia. |
| [PAPER_BAG](#PAPER-BAG) | Texture di sacchetto di carta. |
| [PAPYRUS](#PAPYRUS) | Texture di papiro. |
| [PARCHMENT](#PARCHMENT) | Texture di pergamena. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Texture di carta velina rosa. |
| [PURPLE_MESH](#PURPLE-MESH) | Texture di rete viola. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Texture di carta riciclata. |
| [SAND](#SAND) | Texture di sabbia. |
| [STATIONERY](#STATIONERY) | Texture di cancelleria. |
| [WALNUT](#WALNUT) | Texture di noce. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Texture di gocce d'acqua. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Texture di marmo bianco. |
| [WOVEN_MAT](#WOVEN-MAT) | Texture di tappeto intrecciato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Texture di carta velina blu.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Texture a bouquet.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Texture di marmo marrone.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Texture di tela.

### CORK {#CORK}
```
public static int CORK
```


Texture di sughero.

### DENIM {#DENIM}
```
public static int DENIM
```


Texture di denim.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Texture di fossile di pesce.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Texture di granito.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Texture di marmo verde.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Texture di legno medio.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Texture di carta da giornale.

### NONE {#NONE}
```
public static int NONE
```


Nessuna texture.

### OAK {#OAK}
```
public static int OAK
```


Texture di quercia.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Texture di sacchetto di carta.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Texture di papiro.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Texture di pergamena.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Texture di carta velina rosa.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Texture di rete viola.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Texture di carta riciclata.

### SAND {#SAND}
```
public static int SAND
```


Texture di sabbia.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Texture di cancelleria.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Texture di noce.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Texture di gocce d'acqua.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Texture di marmo bianco.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Texture di tappeto intrecciato.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
