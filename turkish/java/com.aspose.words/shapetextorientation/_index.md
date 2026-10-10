---
title: "ShapeTextOrientation"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words Java için"
description: "Java'da şekillerdeki metnin yönünü belirtir."
type: docs
weight: 617
url: /tr/java/com.aspose.words/shapetextorientation/
---

**Inheritance:**
java.lang.Object
```
public class ShapeTextOrientation
```

Şekillerdeki metnin yönünü belirtir.

 **Examples:** 

Veri etiketlerinin yönelim ve döndürülmesinin nasıl değiştirileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DOWNWARD](#DOWNWARD) | Metin, üstten alta görünmek için 90 derece sağa döndürülür (tb-rl). |
| [HORIZONTAL](#HORIZONTAL) | Metin yatay olarak düzenlenir (lr-tb). |
| [UPWARD](#UPWARD) | Metin, alttan üste görünmek için 90 derece sola döndürülür (bt-lr). |
| [VERTICAL_FAR_EAST](#VERTICAL-FAR-EAST) | Uzak Doğu karakterleri dikey görünür, diğer metin ise üstten alta görünmek için 90 derece sağa döndürülür (tb-rl-v). |
| [VERTICAL_ROTATED_FAR_EAST](#VERTICAL-ROTATED-FAR-EAST) | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa 90 derece döndürülerek yukarıdan aşağıya dikey, ardından soldan sağa yatay olarak görünür (tb-lr-v). |
| [WORD_ART_VERTICAL](#WORD-ART-VERTICAL) | Metin dikeydir, bir harf diğerinin üstünde. |
| [WORD_ART_VERTICAL_RIGHT_TO_LEFT](#WORD-ART-VERTICAL-RIGHT-TO-LEFT) | Metin dikeydir, bir harf diğerinin üstünde, ardından yatay olarak sağdan sola. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String shapeTextOrientationName)](#fromName-java.lang.String) |  |
| [getName(int shapeTextOrientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int shapeTextOrientation)](#toString-int) |  |
### DOWNWARD {#DOWNWARD}
```
public static int DOWNWARD
```


Metin, üstten alta görünmek için 90 derece sağa döndürülür (tb-rl).

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Metin yatay olarak düzenlenir (lr-tb).

### UPWARD {#UPWARD}
```
public static int UPWARD
```


Metin, alttan üste görünmek için 90 derece sola döndürülür (bt-lr).

### VERTICAL_FAR_EAST {#VERTICAL-FAR-EAST}
```
public static int VERTICAL_FAR_EAST
```


Uzak Doğu karakterleri dikey görünür, diğer metin ise üstten alta görünmek için 90 derece sağa döndürülür (tb-rl-v).

### VERTICAL_ROTATED_FAR_EAST {#VERTICAL-ROTATED-FAR-EAST}
```
public static int VERTICAL_ROTATED_FAR_EAST
```


Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa 90 derece döndürülerek yukarıdan aşağıya dikey, ardından soldan sağa yatay olarak görünür (tb-lr-v).

### WORD_ART_VERTICAL {#WORD-ART-VERTICAL}
```
public static int WORD_ART_VERTICAL
```


Metin dikeydir, bir harf diğerinin üstünde.

### WORD_ART_VERTICAL_RIGHT_TO_LEFT {#WORD-ART-VERTICAL-RIGHT-TO-LEFT}
```
public static int WORD_ART_VERTICAL_RIGHT_TO_LEFT
```


Metin dikeydir, bir harf diğerinin üstünde, ardından yatay olarak sağdan sola.

### length {#length}
```
public static int length
```


### fromName(String shapeTextOrientationName) {#fromName-java.lang.String}
```
public static int fromName(String shapeTextOrientationName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeTextOrientationName | java.lang.String |  |

**Returns:**
int
### getName(int shapeTextOrientation) {#getName-int}
```
public static String getName(int shapeTextOrientation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeTextOrientation | int |  |

**Returns:**
java.lang.String
