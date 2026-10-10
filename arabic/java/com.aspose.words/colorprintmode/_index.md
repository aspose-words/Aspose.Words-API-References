---
title: "ColorPrintMode"
linktitle: "ColorPrintMode"
second_title: "Aspose.Words لـ Java"
description: "Specifies how non-colored pages are printed if the device supports color printing in Java."
type: docs
weight: 106
url: /ar/java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

يحدد كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان.
## الحقول

| حقل | الوصف |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Non-colored pages if detected are printed in grayscale. |
| [NORMAL](#NORMAL) | All pages are printed according to the printer's capabilities and settings. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| colorPrintMode | int |  |

**Returns:**
java.lang.String
