---
title: "OdtSaveMeasureUnit"
linktitle: "OdtSaveMeasureUnit"
second_title: "Aspose.Words für Java"
description: "Angegebene Maßeinheiten, die auf messbare Dokumentinhalte wie Formbreiten und andere beim Speichern in Java angewendet werden."
type: docs
weight: 494
url: /de/java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

Angegebene Maßeinheiten, die beim Speichern auf messbaren Dokumentinhalt wie Formen, Breiten und andere angewendet werden.

 **Examples:** 

Zeigt, wie verschiedene Maßeinheiten verwendet werden, um Stilparameter eines gespeicherten ODT-Dokuments zu definieren.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Gibt an, dass der Dokumentinhalt in Zentimetern gespeichert wird. |
| [INCHES](#INCHES) | Gibt an, dass der Dokumentinhalt in Zoll gespeichert wird. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Gibt an, dass der Dokumentinhalt in Zentimetern gespeichert wird.

### INCHES {#INCHES}
```
public static int INCHES
```


Gibt an, dass der Dokumentinhalt in Zoll gespeichert wird.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
