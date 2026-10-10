---
title: "OdtSaveMeasureUnit"
linktitle: "OdtSaveMeasureUnit"
second_title: "Aspose.Words para Java"
description: "Unidades de medida especificadas para aplicar al contenido medible del documento, como anchos de formas y otros, durante el guardado en Java."
type: docs
weight: 494
url: /es/java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

Unidades de medida especificadas para aplicar al contenido medible del documento, como formas, anchuras y otros, durante el guardado.

 **Examples:** 

Muestra cómo usar diferentes unidades de medida para definir parámetros de estilo de un documento ODT guardado.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Especifica que el contenido del documento se guarda usando centímetros. |
| [INCHES](#INCHES) | Especifica que el contenido del documento se guarda usando pulgadas. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Especifica que el contenido del documento se guarda usando centímetros.

### INCHES {#INCHES}
```
public static int INCHES
```


Especifica que el contenido del documento se guarda usando pulgadas.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
