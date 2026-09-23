---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words für Java"
description: "Gibt die Ausrichtung von Text in Formen in Java an."
type: docs
weight: 617
url: /de/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Gibt die Ausrichtung des Textes in Formen an.

 **Examples:** 

Zeigt, wie man die Ausrichtung und Drehung für Datenbeschriftungen ändert.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Der Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Der Text wird horizontal angeordnet (lr-tb). |
| [UPWARD](#UPWARD) | Der Text wird um 90 Grad nach links gedreht, sodass er von unten nach oben erscheint (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er vertikal von oben nach unten erscheint und dann horizontal von links nach rechts (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht, dann horizontal von rechts nach links. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Der Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Der Text wird horizontal angeordnet (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Der Text wird um 90 Grad nach links gedreht, sodass er von unten nach oben erscheint (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Ostasiatische Zeichen erscheinen vertikal, anderer Text wird um 90 Grad nach rechts gedreht, sodass er vertikal von oben nach unten erscheint und dann horizontal von links nach rechts (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht, dann horizontal von rechts nach links.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
