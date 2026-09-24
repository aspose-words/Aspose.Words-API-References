---
title: "RelativeHorizontalSize"
linktitle: "RelativeHorizontalSize"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekil veya metin çerçevesinin genişliğinin yatay olarak neye göre hesaplandığını belirtir."
type: docs
weight: 562
url: /tr/java/com.aspose.words/relativehorizontalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalSize
```

Bir şeklin veya metin çerçevesinin genişliğinin yatay olarak neye göre hesaplandığını belirtir.

 **Examples:** 

Göreceli boyut ve konumun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Adding a simple shape with absolute size and position.
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 40.0);
 // Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
 shape.setWrapType(WrapType.NONE);

 // Checking and setting the relative horizontal size.
 if (shape.getRelativeHorizontalSize() == RelativeHorizontalSize.DEFAULT)
 {
     // Setting the horizontal size binding to Margin.
     shape.setRelativeHorizontalSize(RelativeHorizontalSize.MARGIN);
     // Setting the width to 50% of Margin width.
     shape.setWidthRelative(50f);
 }

 // Checking and setting the relative vertical size.
 if (shape.getRelativeVerticalSize() == RelativeVerticalSize.DEFAULT)
 {
     // Setting the vertical size binding to Margin.
     shape.setRelativeVerticalSize(RelativeVerticalSize.MARGIN);
     // Setting the heigh to 30% of Margin height.
     shape.setHeightRelative(30f);
 }

 // Checking and setting the relative vertical position.
 if (shape.getRelativeVerticalPosition() == RelativeVerticalPosition.PARAGRAPH)
 {
     // etting the position binding to TopMargin.
     shape.setRelativeVerticalPosition(RelativeVerticalPosition.TOP_MARGIN);
     // Setting relative Top to 30% of TopMargin position.
     shape.setTopRelative(30f);
 }

 // Checking and setting the relative horizontal position.
 if (shape.getRelativeHorizontalPosition() == RelativeHorizontalPosition.DEFAULT)
 {
     // Setting the position binding to RightMargin.
     shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.RIGHT_MARGIN);
     // The position relative value can be negative.
     shape.setLeftRelative(-260);
 }

 doc.save(getArtifactsDir() + "Shape.RelativeSizeAndPosition.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DEFAULT](#DEFAULT) | Varsayılan değer [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN)'dır. |
| [INNER_MARGIN](#INNER-MARGIN) | Genişliğin, iç kenar boşluğu alanının boyutuna, tek sayfalarda sol kenar boşluğu alanının boyutuna ve çift sayfalarda sağ kenar boşluğu alanının boyutuna göre hesaplandığını belirtir. |
| [LEFT_MARGIN](#LEFT-MARGIN) | Genişliğin sol kenar boşluğu alanının boyutuna göre hesaplandığını belirtir. |
| [MARGIN](#MARGIN) | Genişliğin sol ve sağ kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Genişliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için sağ kenar boşluğu alanı boyutuna ve çift sayfalar için sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [PAGE](#PAGE) | Genişliğin sayfa genişliğine göre hesaplandığını belirtir. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Genişliğin sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String relativeHorizontalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalSize)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [MARGIN](../../com.aspose.words/relativehorizontalsize/\#MARGIN)'dır.

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Genişliğin, iç kenar boşluğu alanının boyutuna, tek sayfalarda sol kenar boşluğu alanının boyutuna ve çift sayfalarda sağ kenar boşluğu alanının boyutuna göre hesaplandığını belirtir.

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Genişliğin sol kenar boşluğu alanının boyutuna göre hesaplandığını belirtir.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Genişliğin sol ve sağ kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Genişliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için sağ kenar boşluğu alanı boyutuna ve çift sayfalar için sol kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### PAGE {#PAGE}
```
public static int PAGE
```


Genişliğin sayfa genişliğine göre hesaplandığını belirtir.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Genişliğin sağ kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalSizeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalSize) {#getName-int}
```
public static String getName(int relativeHorizontalSize)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalSize) {#toString-int}
```
public static String toString(int relativeHorizontalSize)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalSize | int |  |

**Returns:**
java.lang.String
