---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words Java için"
description: "Cihaz Java'da renkli baskıyı destekliyorsa, renksiz sayfaların nasıl yazdırılacağını belirtir."
type: docs
weight: 106
url: /tr/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Cihaz renkli baskıyı destekliyorsa, renksiz sayfaların nasıl yazdırılacağını belirtir.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Algılanan renksiz sayfalar gri tonlamada yazdırılır. |
| [NORMAL](#NORMAL) | Tüm sayfalar yazıcının yetenekleri ve ayarlarına göre yazdırılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Algılanan renksiz sayfalar gri tonlamada yazdırılır.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) algılanan renksiz sayfalar için otomatik olarak false olarak ayarlanır. Yazıcı renkli baskıyı desteklemiyorsa, bu ayar yoksayılır.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Tüm sayfalar yazıcının yetenekleri ve ayarlarına göre yazdırılır.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorPrintMode) {#toString-int}
```
public static String toString(int colorPrintMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
