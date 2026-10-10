---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie nicht‑farbige Seiten gedruckt werden, wenn das Gerät das Farb‑Drucken in Java unterstützt."
type: docs
weight: 106
url: /de/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Gibt an, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Nicht‑farbige Seiten werden, falls erkannt, in Graustufen gedruckt. |
| [NORMAL](#NORMAL) | Alle Seiten werden gemäß den Fähigkeiten und Einstellungen des Druckers gedruckt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Nicht‑farbige Seiten werden, falls erkannt, in Graustufen gedruckt.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) wird für erkannte nicht‑farbige Seiten automatisch auf false gesetzt. Wenn der Drucker das Farb‑Drucken nicht unterstützt, wird diese Einstellung ignoriert.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Alle Seiten werden gemäß den Fähigkeiten und Einstellungen des Druckers gedruckt.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
