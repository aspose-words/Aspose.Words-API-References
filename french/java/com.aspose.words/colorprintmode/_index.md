---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les pages non colorées sont imprimées si l'appareil prend en charge l'impression couleur en Java."
type: docs
weight: 106
url: /fr/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Spécifie comment les pages non colorées sont imprimées si l'appareil prend en charge l'impression couleur.
## Champs

| Champ | Description |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Les pages non colorées, si détectées, sont imprimées en niveaux de gris. |
| [NORMAL](#NORMAL) | Toutes les pages sont imprimées selon les capacités et les paramètres de l'imprimante. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Les pages non colorées, si détectées, sont imprimées en niveaux de gris.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) est automatiquement réglé sur false pour les pages non colorées détectées. Si l'imprimante ne prend pas en charge l'impression couleur, ce paramètre est ignoré.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Toutes les pages sont imprimées selon les capacités et les paramètres de l'imprimante.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
