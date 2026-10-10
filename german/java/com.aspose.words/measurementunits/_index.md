---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words für Java"
description: "Gibt die Maßeinheit in Java an."
type: docs
weight: 460
url: /de/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Gibt die Maßeinheit an.

 **Examples:** 

Zeigt, wie ein gespeichertes Dokument einem älteren ODT-Schema entspricht.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Zentimeter. |
| [INCHES](#INCHES) | Zoll. |
| [MILLIMETERS](#MILLIMETERS) | Millimeter. |
| [PICAS](#PICAS) | Picas (häufig verwendet bei traditioneller Schreibmaschinenschriftabstand). |
| [POINTS](#POINTS) | Punkte. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Zentimeter.

### INCHES {#INCHES}
```
public static int INCHES
```


Zoll.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Millimeter.

### PICAS {#PICAS}
```
public static int PICAS
```


Picas (häufig verwendet bei traditioneller Schreibmaschinenschriftabstand).

### POINTS {#POINTS}
```
public static int POINTS
```


Punkte.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int measurementUnits) {#toString-int}
```
public static String toString(int measurementUnits)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
