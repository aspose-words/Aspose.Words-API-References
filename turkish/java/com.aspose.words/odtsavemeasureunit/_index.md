---
title: "OdtSaveMeasureUnit"
linktitle: "OdtSaveMeasureUnit"
second_title: "Aspose.Words Java için"
description: "Java'da kaydetme sırasında şekil genişlikleri ve diğer ölçülebilir belge içeriğine uygulanacak belirtilen ölçü birimleri."
type: docs
weight: 494
url: /tr/java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

Kaydetme sırasında şekil, genişlikler ve diğer ölçülebilir belge içeriğine uygulanacak belirtilen ölçü birimleri.

 **Examples:** 

Kaydedilmiş bir ODT belgesinin stil parametrelerini tanımlamak için farklı ölçü birimlerinin nasıl kullanılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | Belgenin içeriğinin santimetre kullanılarak kaydedildiğini belirtir. |
| [INCHES](#INCHES) | Belgenin içeriğinin inç kullanılarak kaydedildiğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


Belgenin içeriğinin santimetre kullanılarak kaydedildiğini belirtir.

### INCHES {#INCHES}
```
public static int INCHES
```


Belgenin içeriğinin inç kullanılarak kaydedildiğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
