---
title: "BorderType"
linktitle: "BorderType"
second_title: "Aspose.Words Java için"
description: "Java'da bir kenarlığın kenarlarını belirtir."
type: docs
weight: 48
url: /tr/java/com.aspose.words/bordertype/
---

**Inheritance:**
java.lang.Object
```
public class BorderType
```

Bir kenarlığın taraflarını belirtir.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Üst kenarlı bir paragraf eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Border topBorder = builder.getParagraphFormat().getBorders().getByBorderType(BorderType.TOP);
 topBorder.setLineWidth(4.0d);
 topBorder.setLineStyle(LineStyle.DASH_SMALL_GAP);
 // Set ThemeColor only when LineWidth or LineStyle setted.
 topBorder.setThemeColor(ThemeColor.ACCENT_1);
 topBorder.setTintAndShade(0.25d);

 builder.writeln("Text with a top border.");

 doc.save(getArtifactsDir() + "Border.ParagraphTopBorder.docx");
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTTOM](#BOTTOM) | Bir paragrafın veya tablo hücresinin alt kenarlığını belirtir. |
| [DIAGONAL_DOWN](#DIAGONAL-DOWN) | Bir tablo hücresindeki çapraz kenarı belirtir. |
| [DIAGONAL_UP](#DIAGONAL-UP) | Bir tablo hücresindeki çapraz kenarı belirtir. |
| [HORIZONTAL](#HORIZONTAL) | Bir tablo içindeki hücreler arasında veya uyumlu paragraflar arasında yatay kenarı belirtir. |
| [LEFT](#LEFT) | Bir paragrafın veya tablo hücresinin sol kenarını belirtir. |
| [NONE](#NONE) | Varsayılan değer. |
| [RIGHT](#RIGHT) | Bir paragrafın veya tablo hücresinin sağ kenarını belirtir. |
| [TOP](#TOP) | Bir paragrafın veya tablo hücresinin üst kenarını belirtir. |
| [VERTICAL](#VERTICAL) | Bir tablo içindeki hücreler arasında dikey kenarı belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String borderTypeName)](#fromName-java.lang.String) |  |
| [getName(int borderType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int borderType)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Bir paragrafın veya tablo hücresinin alt kenarlığını belirtir.

### DIAGONAL_DOWN {#DIAGONAL-DOWN}
```
public static int DIAGONAL_DOWN
```


Bir tablo hücresindeki çapraz kenarı belirtir.

### DIAGONAL_UP {#DIAGONAL-UP}
```
public static int DIAGONAL_UP
```


Bir tablo hücresindeki çapraz kenarı belirtir.

### HORIZONTAL {#HORIZONTAL}
```
public static int HORIZONTAL
```


Bir tablo içindeki hücreler arasında veya uyumlu paragraflar arasında yatay kenarı belirtir.

### LEFT {#LEFT}
```
public static int LEFT
```


Bir paragrafın veya tablo hücresinin sol kenarını belirtir.

### NONE {#NONE}
```
public static int NONE
```


Varsayılan değer.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Bir paragrafın veya tablo hücresinin sağ kenarını belirtir.

### TOP {#TOP}
```
public static int TOP
```


Bir paragrafın veya tablo hücresinin üst kenarını belirtir.

### VERTICAL {#VERTICAL}
```
public static int VERTICAL
```


Bir tablo içindeki hücreler arasında dikey kenarı belirtir.

### length {#length}
```
public static int length
```


### fromName(String borderTypeName) {#fromName-java.lang.String}
```
public static int fromName(String borderTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderTypeName | java.lang.String |  |

**Returns:**
int
### getName(int borderType) {#getName-int}
```
public static String getName(int borderType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int borderType) {#toString-int}
```
public static String toString(int borderType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderType | int |  |

**Returns:**
java.lang.String
