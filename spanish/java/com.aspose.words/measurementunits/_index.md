---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words para Java"
description: "Especifica la unidad de medida en Java."
type: docs
weight: 460
url: /es/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Especifica la unidad de medida.

 **Examples:** 

Muestra cómo hacer que un documento guardado cumpla con un esquema ODT más antiguo.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Centímetros. |
| [INCHES](#INCHES) | Pulgadas. |
| [MILLIMETERS](#MILLIMETERS) | Milímetros. |
| [PICAS](#PICAS) | Picas (comúnmente usadas en el espaciado de fuentes de máquinas de escribir tradicionales). |
| [POINTS](#POINTS) | Puntos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Centímetros.

### INCHES {#INCHES}
```
public static int INCHES
```


Pulgadas.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Milímetros.

### PICAS {#PICAS}
```
public static int PICAS
```


Picas (comúnmente usadas en el espaciado de fuentes de máquinas de escribir tradicionales).

### POINTS {#POINTS}
```
public static int POINTS
```


Puntos.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
