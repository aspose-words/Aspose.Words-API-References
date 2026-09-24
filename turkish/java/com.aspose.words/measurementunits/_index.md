---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words Java için"
description: "Java'da ölçü birimini belirtir."
type: docs
weight: 460
url: /tr/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

Ölçüm birimini belirtir.

 **Examples:** 

Kaydedilmiş bir belgenin eski bir ODT şemasına uymasını nasıl sağlayacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Santimetre. |
| [INCHES](#INCHES) | İnç. |
| [MILLIMETERS](#MILLIMETERS) | Milimetre. |
| [PICAS](#PICAS) | Pika (geleneksel daktilo yazı tipi aralığında yaygın olarak kullanılır). |
| [POINTS](#POINTS) | Puan. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Santimetre.

### INCHES {#INCHES}
```
public static int INCHES
```


İnç.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


Milimetre.

### PICAS {#PICAS}
```
public static int PICAS
```


Pika (geleneksel daktilo yazı tipi aralığında yaygın olarak kullanılır).

### POINTS {#POINTS}
```
public static int POINTS
```


Puan.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
