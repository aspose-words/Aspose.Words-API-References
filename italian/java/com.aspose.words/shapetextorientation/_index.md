---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words per Java"
description: "Specifica l'orientamento del testo nelle forme in Java."
type: docs
weight: 617
url: /it/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Specifica l'orientamento del testo nelle forme.

 **Examples:** 

Mostra come modificare l'orientamento e la rotazione delle etichette dati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Il testo è disposto orizzontalmente (lr-tb). |
| [UPWARD](#UPWARD) | Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | Il testo è verticale, con una lettera sopra l'altra. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | Il testo è verticale, con una lettera sopra l'altra, poi da destra a sinistra in orizzontale. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Il testo è disposto orizzontalmente (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


Il testo è verticale, con una lettera sopra l'altra.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


Il testo è verticale, con una lettera sopra l'altra, poi da destra a sinistra in orizzontale.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int shapeTextOrientation) {#toString-int}
```
public static String toString(int shapeTextOrientation)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
