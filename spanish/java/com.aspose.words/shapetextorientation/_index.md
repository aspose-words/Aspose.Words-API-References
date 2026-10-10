---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words para Java"
description: "Especifica la orientación del texto en formas en Java."
type: docs
weight: 617
url: /es/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Especifica la orientación del texto en las formas.

 **Examples:** 

Muestra cómo cambiar la orientación y la rotación de las etiquetas de datos.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | El texto se dispone horizontalmente (lr-tb). |
| [UPWARD](#UPWARD) | El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Los caracteres de Extremo Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto está rotado 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | El texto es vertical, con una letra encima de la otra. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | El texto es vertical, con una letra encima de la otra, luego de derecha a izquierda horizontalmente. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


El texto se dispone horizontalmente (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Los caracteres de Extremo Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Los caracteres del Lejano Oriente aparecen verticales, el resto del texto está rotado 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


El texto es vertical, con una letra encima de la otra.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


El texto es vertical, con una letra encima de la otra, luego de derecha a izquierda horizontalmente.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
