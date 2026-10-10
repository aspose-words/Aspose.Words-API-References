---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'unité de mesure en Java."
type: docs
weight: 460
url: /fr/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Spécifie l'unité de mesure.

 **Examples:** 

Montre comment faire conformer un document enregistré à un schéma ODT plus ancien.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Centimètres. |
| [INCHES](#INCHES) | Pouces. |
| [MILLIMETERS](#MILLIMETERS) | Millimètres. |
| [PICAS](#PICAS) | Picas (couramment utilisés dans l'espacement des polices de machine à écrire traditionnelle). |
| [POINTS](#POINTS) | Points. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Centimètres.

### INCHES {#INCHES}
```
public static int INCHES
```


Pouces.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Millimètres.

### PICAS {#PICAS}
```
public static int PICAS
```


Picas (couramment utilisés dans l'espacement des polices de machine à écrire traditionnelle).

### POINTS {#POINTS}
```
public static int POINTS
```


Points.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
