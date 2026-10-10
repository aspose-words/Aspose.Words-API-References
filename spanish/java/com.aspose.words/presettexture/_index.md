---
title: "PresetTexture"
linktitle: "PresetTexture"
second_title: "Aspose.Words para Java"
description: "Especifica la textura que se usará para rellenar una forma en Java."
type: docs
weight: 552
url: /es/java/com.aspose.words/presettexture/
---

**Inheritance:**
java.lang.Object
```
public class PresetTexture
```

Especifica la textura que se usará para rellenar una forma.

 **Examples:** 

Muestra cómo establecer el formato del marcador.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BLUE_TISSUE_PAPER](#BLUE-TISSUE-PAPER) | Textura de papel tisú azul. |
| [BOUQUET](#BOUQUET) | Textura de ramo. |
| [BROWN_MARBLE](#BROWN-MARBLE) | Textura de mármol marrón. |
| [CANVAS](#CANVAS) | Textura de lienzo. |
| [CORK](#CORK) | Textura de corcho. |
| [DENIM](#DENIM) | Textura de mezclilla. |
| [FISH_FOSSIL](#FISH-FOSSIL) | Textura de fósil de pez. |
| [GRANITE](#GRANITE) | Textura de granito. |
| [GREEN_MARBLE](#GREEN-MARBLE) | Textura de mármol verde. |
| [MEDIUM_WOOD](#MEDIUM-WOOD) | Textura de madera mediana. |
| [NEWSPRINT](#NEWSPRINT) | Textura de papel de periódico. |
| [NONE](#NONE) | Sin textura. |
| [OAK](#OAK) | Textura de roble. |
| [PAPER_BAG](#PAPER-BAG) | Textura de bolsa de papel. |
| [PAPYRUS](#PAPYRUS) | Textura de papiro. |
| [PARCHMENT](#PARCHMENT) | Textura de pergamino. |
| [PINK_TISSUE_PAPER](#PINK-TISSUE-PAPER) | Textura de papel tisú rosa. |
| [PURPLE_MESH](#PURPLE-MESH) | Textura de malla púrpura. |
| [RECYCLED_PAPER](#RECYCLED-PAPER) | Textura de papel reciclado. |
| [SAND](#SAND) | Textura de arena. |
| [STATIONERY](#STATIONERY) | Textura de papelería. |
| [WALNUT](#WALNUT) | Textura de nogal. |
| [WATER_DROPLETS](#WATER-DROPLETS) | Textura de gotas de agua. |
| [WHITE_MARBLE](#WHITE-MARBLE) | Textura de mármol blanco. |
| [WOVEN_MAT](#WOVEN-MAT) | Textura de alfombra tejida. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String presetTextureName)](#fromName-java.lang.String) |  |
| [getName(int presetTexture)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int presetTexture)](#toString-int) |  |
### BLUE_TISSUE_PAPER {#BLUE-TISSUE-PAPER}
```
public static int BLUE_TISSUE_PAPER
```


Textura de papel tisú azul.

### BOUQUET {#BOUQUET}
```
public static int BOUQUET
```


Textura de ramo.

### BROWN_MARBLE {#BROWN-MARBLE}
```
public static int BROWN_MARBLE
```


Textura de mármol marrón.

### CANVAS {#CANVAS}
```
public static int CANVAS
```


Textura de lienzo.

### CORK {#CORK}
```
public static int CORK
```


Textura de corcho.

### DENIM {#DENIM}
```
public static int DENIM
```


Textura de mezclilla.

### FISH_FOSSIL {#FISH-FOSSIL}
```
public static int FISH_FOSSIL
```


Textura de fósil de pez.

### GRANITE {#GRANITE}
```
public static int GRANITE
```


Textura de granito.

### GREEN_MARBLE {#GREEN-MARBLE}
```
public static int GREEN_MARBLE
```


Textura de mármol verde.

### MEDIUM_WOOD {#MEDIUM-WOOD}
```
public static int MEDIUM_WOOD
```


Textura de madera mediana.

### NEWSPRINT {#NEWSPRINT}
```
public static int NEWSPRINT
```


Textura de papel de periódico.

### NONE {#NONE}
```
public static int NONE
```


Sin textura.

### OAK {#OAK}
```
public static int OAK
```


Textura de roble.

### PAPER_BAG {#PAPER-BAG}
```
public static int PAPER_BAG
```


Textura de bolsa de papel.

### PAPYRUS {#PAPYRUS}
```
public static int PAPYRUS
```


Textura de papiro.

### PARCHMENT {#PARCHMENT}
```
public static int PARCHMENT
```


Textura de pergamino.

### PINK_TISSUE_PAPER {#PINK-TISSUE-PAPER}
```
public static int PINK_TISSUE_PAPER
```


Textura de papel tisú rosa.

### PURPLE_MESH {#PURPLE-MESH}
```
public static int PURPLE_MESH
```


Textura de malla púrpura.

### RECYCLED_PAPER {#RECYCLED-PAPER}
```
public static int RECYCLED_PAPER
```


Textura de papel reciclado.

### SAND {#SAND}
```
public static int SAND
```


Textura de arena.

### STATIONERY {#STATIONERY}
```
public static int STATIONERY
```


Textura de papelería.

### WALNUT {#WALNUT}
```
public static int WALNUT
```


Textura de nogal.

### WATER_DROPLETS {#WATER-DROPLETS}
```
public static int WATER_DROPLETS
```


Textura de gotas de agua.

### WHITE_MARBLE {#WHITE-MARBLE}
```
public static int WHITE_MARBLE
```


Textura de mármol blanco.

### WOVEN_MAT {#WOVEN-MAT}
```
public static int WOVEN_MAT
```


Textura de alfombra tejida.

### length {#length}
```
public static int length
```


### fromName(String presetTextureName) {#fromName-java.lang.String}
```
public static int fromName(String presetTextureName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| presetTextureName | java.lang.String |  |

**Returns:**
int
### getName(int presetTexture) {#getName-int}
```
public static String getName(int presetTexture)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| presetTexture | int |  |

**Returns:**
java.lang.String
