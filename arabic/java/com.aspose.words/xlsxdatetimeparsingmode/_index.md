---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت في Java."
type: docs
weight: 742
url: /ar/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

يحدد كيفية تحليل نص المستند لتحديد قيم التاريخ والوقت.

 **Examples:** 

يظهر كيفية تحديد الكشف التلقائي لتنسيق التاريخ والوقت.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | يتم تحديد تنسيق التاريخ والوقت المستخدم في المستند تلقائيًا. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | يُستخدم تنسيق التاريخ والوقت المحدد للخيط الحالي أولاً لتحليل قيم السلسلة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


يتم تحديد تنسيق التاريخ والوقت المستخدم في المستند تلقائيًا. قد يستغرق ذلك وقتًا إضافيًا.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


يُستخدم تنسيق التاريخ والوقت المحدد للخيط الحالي أولاً لتحليل قيم السلسلة. إذا فشل التحليل، يتم تجربة تنسيقات تاريخ ووقت شائعة أخرى.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
