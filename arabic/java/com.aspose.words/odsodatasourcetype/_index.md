---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO في جافا."
type: docs
weight: 488
url: /ar/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

يحدد نوع مصدر البيانات الخارجي الذي سيتم الاتصال به كجزء من معلومات اتصال ODSO.

 **Remarks:** 

المواصفة OOXML غير واضحة جدًا لهذا التعداد. أعتقد أنها قد تتطابق مع تعداد WdMergeSubType http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## الحقول

| حقل | الوصف |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | يحدد أن المستند المحدد قد تم ربطه بدفتر عناوين للاتصالات. |
| [DATABASE](#DATABASE) | يحدد أن المستند المحدد قد تم ربطه بقاعدة بيانات. |
| [DEFAULT](#DEFAULT) | يساوي [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE). |
| [DOCUMENT_1](#DOCUMENT-1) | يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى يدعمها التطبيق المنتج. |
| [DOCUMENT_2](#DOCUMENT-2) | يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى يدعمها التطبيق المنتج. |
| [EMAIL](#EMAIL) | يحدد أن المستند المحدد قد تم ربطه بتطبيق بريد إلكتروني. |
| [LEGACY](#LEGACY) | يحدد أن المستند المحدد قد تم ربطه بصيغة مستند قديمة يدعمها التطبيق المنتج ربما wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | يحدد أن المستند المحدد قد تم ربطه بمصدر بيانات يجمع مصادر بيانات أخرى. |
| [NATIVE](#NATIVE) | يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى أصلية للتطبيق المنتج. |
| [NONE](#NONE) | نوع مصدر البيانات الخارجي غير محدد. |
| [TEXT](#TEXT) | يحدد أن المستند المحدد قد تم ربطه بملف نصي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


يحدد أن المستند المحدد قد تم ربطه بدفتر عناوين للاتصالات ربما wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


يحدد أن المستند المحدد قد تم ربطه بقاعدة بيانات ربما wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يساوي [NONE](../../com.aspose.words/odsodatasourcetype/\#NONE).

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى يدعمها التطبيق المنتج ربما wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى يدعمها التطبيق المنتج ربما wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


يحدد أن المستند المحدد قد تم ربطه بتطبيق بريد إلكتروني ربما wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


يحدد أن المستند المحدد قد تم ربطه بصيغة مستند قديمة يدعمها التطبيق المنتج ربما wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


يحدد أن المستند المحدد قد تم ربطه بمصدر بيانات يجمع مصادر بيانات أخرى.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


يحدد أن المستند المحدد قد تم ربطه بصيغة مستند أخرى أصلية للتطبيق المنتج ربما wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


نوع مصدر البيانات الخارجي غير محدد ربما wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


يحدد أن المستند المحدد قد تم ربطه بملف نصي ربما wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
