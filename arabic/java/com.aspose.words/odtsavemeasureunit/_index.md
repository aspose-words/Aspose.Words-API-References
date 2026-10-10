---
title: "OdtSaveMeasureUnit"
linktitle: "OdtSaveMeasureUnit"
second_title: "Aspose.Words لـ Java"
description: "الوحدات المحددة للقياس لتطبيقها على محتوى المستند القابل للقياس مثل عرض الأشكال وغيرها أثناء الحفظ في Java."
type: docs
weight: 494
url: /ar/java/com.aspose.words/odtsavemeasureunit/
---

**Inheritance:**
java.lang.Object
```
public class OdtSaveMeasureUnit
```

وحدات القياس المحددة لتطبيقها على محتوى المستند القابل للقياس مثل الشكل والعروض وغيرها أثناء الحفظ.

 **Examples:** 

يوضح كيفية استخدام وحدات قياس مختلفة لتحديد معلمات النمط في مستند ODT المحفوظ.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CENTIMETERS](#CENTIMETERS) | يحدد أن محتوى المستند يُحفظ باستخدام السنتيمترات. |
| [INCHES](#INCHES) | يحدد أن محتوى المستند يُحفظ باستخدام البوصات. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String odtSaveMeasureUnitName)](#fromName-java.lang.String) |  |
| [getName(int odtSaveMeasureUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odtSaveMeasureUnit)](#toString-int) |  |
### CENTIMETERS {#CENTIMETERS}
```
public static int CENTIMETERS
```


يحدد أن محتوى المستند يُحفظ باستخدام السنتيمترات.

### INCHES {#INCHES}
```
public static int INCHES
```


يحدد أن محتوى المستند يُحفظ باستخدام البوصات.

### length {#length}
```
public static int length
```


### fromName(String odtSaveMeasureUnitName) {#fromName-java.lang.String}
```
public static int fromName(String odtSaveMeasureUnitName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| odtSaveMeasureUnitName | java.lang.String |  |

**Returns:**
int
### getName(int odtSaveMeasureUnit) {#getName-int}
```
public static String getName(int odtSaveMeasureUnit)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| odtSaveMeasureUnit | int |  |

**Returns:**
java.lang.String
