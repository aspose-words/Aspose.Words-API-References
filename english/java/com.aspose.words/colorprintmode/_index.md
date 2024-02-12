---
title: ColorPrintMode
linktitle: ColorPrintMode
second_title: Aspose.Words for Java
description: Specifies how non-colored pages are printed if the device supports color printing in Java.
type: docs
weight: 92
url: /java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Specifies how non-colored pages are printed if the device supports color printing.
## Fields

| Field | Description |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Non-colored pages if detected are printed in grayscale. |
| [NORMAL](#NORMAL) | All pages are printed according to the printer's capabilities and settings. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Non-colored pages if detected are printed in grayscale.

 **Remarks:** 

PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) is automatically set false for detected non-colored pages. If the printer does not support color printing, this setting is ignored.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


All pages are printed according to the printer's capabilities and settings.

### length {#length}
```
public static int length
```


### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
