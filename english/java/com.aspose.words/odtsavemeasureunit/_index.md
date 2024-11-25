---
title: OdtSaveMeasureUnit
linktitle: OdtSaveMeasureUnit
second_title: Aspose.Words for Java
description: Specified units of measure to apply to measurable document content such as shape widths and other during saving in Java.
type: docs
weight: 470
url: /java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

Specified units of measure to apply to measurable document content such as shape, widths and other during saving.

 **Examples:** 

Shows how to use different measurement units to define style parameters of a saved ODT document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // When we export the document to .odt, we can use an OdtSaveOptions object to modify how we save the document.
 // We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Centimeters"
 // to define content such as style parameters using the metric system, which Open Office uses.
 // We can set the "MeasureUnit" property to "OdtSaveMeasureUnit.Inches"
 // to define content such as style parameters using the imperial system, which Microsoft Word uses.
 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(odtSaveMeasureUnit);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Specifies that the document content is saved using centimeters. |
| [INCHES](#INCHES) | Specifies that the document content is saved using inches. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Specifies that the document content is saved using centimeters.

### INCHES {#INCHES}
```
public static int INCHES
```


Specifies that the document content is saved using inches.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odtSaveMeasureUnit) {#toString-int}
```
public static String toString(int odtSaveMeasureUnit)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
