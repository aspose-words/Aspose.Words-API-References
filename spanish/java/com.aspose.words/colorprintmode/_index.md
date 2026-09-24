---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se imprimen las páginas sin color si el dispositivo admite impresión en color en Java."
type: docs
weight: 106
url: /es/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Especifica cómo se imprimen las páginas sin color si el dispositivo admite impresión en color.
## Campos

| Campo | Descripción |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Las páginas sin color, si se detectan, se imprimen en escala de grises. |
| [NORMAL](#NORMAL) | Todas las páginas se imprimen de acuerdo con las capacidades y configuraciones de la impresora. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Las páginas sin color, si se detectan, se imprimen en escala de grises.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) se establece automáticamente en false para las páginas sin color detectadas. Si la impresora no admite impresión en color, esta configuración se ignora.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Todas las páginas se imprimen de acuerdo con las capacidades y configuraciones de la impresora.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
