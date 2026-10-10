---
title: "MeasurementUnits"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words لـ Java"
description: "يحدد وحدة القياس في Java."
type: docs
weight: 460
url: /ar/java/com.aspose.words/measurementunits/
---

**Inheritance:**
java.lang.Object
```
public class MeasurementUnits
```

يحدد وحدة القياس.

 **Examples:** 

يعرض كيفية جعل المستند المحفوظ يتوافق مع مخطط ODT أقدم.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 OdtSaveOptions saveOptions = new OdtSaveOptions();
 {
     saveOptions.setMeasureUnit(OdtSaveMeasureUnit.CENTIMETERS);
     saveOptions.isStrictSchema11(exportToOdt11Specs);
 }

 doc.save(getArtifactsDir() + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | سنتيمترات. |
| [INCHES](#INCHES) | بوصات. |
| [MILLIMETERS](#MILLIMETERS) | ملليمترات. |
| [PICAS](#PICAS) | بيكات (تُستخدم عادةً في تباعد خطوط الآلة الكاتبة التقليدية). |
| [POINTS](#POINTS) | نقاط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String measurementUnitsName)](#fromName-java.lang.String) |  |
| [getName(int measurementUnits)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int measurementUnits)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


سنتيمترات.

### INCHES {#INCHES}
```
public static int INCHES
```


بوصات.

### MILLIMETERS {#MILLIMETERS}
```
public static int MILLIMETERS
```


ملليمترات.

### PICAS {#PICAS}
```
public static int PICAS
```


بيكات (تُستخدم عادةً في تباعد خطوط الآلة الكاتبة التقليدية).

### POINTS {#POINTS}
```
public static int POINTS
```


نقاط.

### length {#length}
```
public static int length
```


### fromName(String measurementUnitsName) {#fromName-java.lang.String}
```
public static int fromName(String measurementUnitsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| measurementUnitsName | java.lang.String |  |

**Returns:**
int
### getName(int measurementUnits) {#getName-int}
```
public static String getName(int measurementUnits)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| measurementUnits | int |  |

**Returns:**
java.lang.String
