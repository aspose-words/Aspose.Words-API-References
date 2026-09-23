---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words per Java"
description: "Specifica l'unità di misura in Java."
type: docs
weight: 460
url: /it/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Specifica l'unità di misura.

 **Examples:** 

Mostra come far conformare un documento salvato a uno schema ODT più vecchio.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Centimetri. |
| [INCHES](#INCHES) | Pollici. |
| [MILLIMETERS](#MILLIMETERS) | Millimetri. |
| [PICAS](#PICAS) | Piche (comunemente usate nella spaziatura dei caratteri delle macchine da scrivere tradizionali). |
| [POINTS](#POINTS) | Punti. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Centimetri.

### INCHES {#INCHES}
```
public static int INCHES
```


Pollici.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Millimetri.

### PICAS {#PICAS}
```
public static int PICAS
```


Piche (comunemente usate nella spaziatura dei caratteri delle macchine da scrivere tradizionali).

### POINTS {#POINTS}
```
public static int POINTS
```


Punti.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
