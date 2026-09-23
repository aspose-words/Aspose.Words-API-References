---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'orientation du texte dans les formes en Java."
type: docs
weight: 617
url: /fr/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Spécifie l'orientation du texte dans les formes.

 **Examples:** 

Montre comment modifier l'orientation et la rotation des étiquettes de données.

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
## Champs

| Champ | Description |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Le texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Le texte est disposé horizontalement (lr-tb). |
| [UPWARD](#UPWARD) | Le texte est tourné de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est tourné de 90 degrés vers la droite pour s'afficher de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | Le texte est vertical, avec une lettre au-dessus de l'autre. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | Le texte est vertical, avec une lettre au-dessus de l'autre, puis de droite à gauche horizontalement. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Le texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Le texte est disposé horizontalement (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Le texte est tourné de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Les caractères d'Extrême-Orient apparaissent verticalement, le reste du texte est tourné de 90 degrés vers la droite pour s'afficher de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


Le texte est vertical, avec une lettre au-dessus de l'autre.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


Le texte est vertical, avec une lettre au-dessus de l'autre, puis de droite à gauche horizontalement.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
