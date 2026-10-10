---
title: "RelativeVerticalSize"
linktitle: "RelativeVerticalSize"
second_title: "Aspose.Words Java için"
description: "Java'da bir şeklin veya metin çerçevesinin yüksekliğinin dikey olarak neye göre hesaplandığını belirtir."
type: docs
weight: 564
url: /tr/java/com.aspose.words/relativeverticalsize/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalSize
```

Bir şeklin veya metin çerçevesinin yüksekliğinin dikey olarak neye göre hesaplandığını belirtir.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Yüksekliğin alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [DEFAULT](#DEFAULT) | Varsayılan değer [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN). |
| [INNER_MARGIN](#INNER-MARGIN) | Yüksekliğin iç kenar boşluğu alanı boyutuna, tek sayfalar için üst kenar boşluğu alanı boyutuna ve çift sayfalar için alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [MARGIN](#MARGIN) | Yüksekliğin üst ve alt kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir. |
| [OUTER_MARGIN](#OUTER-MARGIN) | Yüksekliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için alt kenar boşluğu alanı boyutuna ve çift sayfalar için üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [PAGE](#PAGE) | Yüksekliğin sayfa yüksekliğine göre hesaplandığını belirtir. |
| [TOP_MARGIN](#TOP-MARGIN) | Yüksekliğin üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String relativeVerticalSizeName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalSize)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Yüksekliğin alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [MARGIN](../../com.aspose.words/relativeverticalsize/\#MARGIN).

### INNER_MARGIN {#INNER-MARGIN}
```
public static int INNER_MARGIN
```


Yüksekliğin iç kenar boşluğu alanı boyutuna, tek sayfalar için üst kenar boşluğu alanı boyutuna ve çift sayfalar için alt kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Yüksekliğin üst ve alt kenar boşlukları arasındaki boşluğa göre hesaplandığını belirtir.

### OUTER_MARGIN {#OUTER-MARGIN}
```
public static int OUTER_MARGIN
```


Yüksekliğin dış kenar boşluğu alanı boyutuna, tek sayfalar için alt kenar boşluğu alanı boyutuna ve çift sayfalar için üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### PAGE {#PAGE}
```
public static int PAGE
```


Yüksekliğin sayfa yüksekliğine göre hesaplandığını belirtir.

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Yüksekliğin üst kenar boşluğu alanı boyutuna göre hesaplandığını belirtir.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalSizeName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalSizeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalSizeName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalSize) {#getName-int}
```
public static String getName(int relativeVerticalSize)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalSize) {#toString-int}
```
public static String toString(int relativeVerticalSize)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalSize | int |  |

**Returns:**
java.lang.String
