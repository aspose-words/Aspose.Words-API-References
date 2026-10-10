---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع مصدر بيانات دمج البريد الخارجي في Java."
type: docs
weight: 440
url: /ar/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

يحدد نوع مصدر بيانات دمج البريد الخارجي.
## الحقول

| حقل | الوصف |
| --- | --- |
| [DATABASE](#DATABASE) | يحدد أن المستند المحدد تم ربطه بقاعدة بيانات Access عبر نظام تبادل البيانات الديناميكي (DDE). |
| [DEFAULT](#DEFAULT) | يساوي [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي عبر واجهة كائن مصدر بيانات المكتب (ODSO). |
| [NONE](#NONE) | لم يتم تحديد مصدر بيانات دمج البريد. |
| [ODBC](#ODBC) | يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي عبر واجهة Open Database Connectivity. |
| [QUERY](#QUERY) | يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي باستخدام أداة استعلام خارجية. |
| [SPREADSHEET](#SPREADSHEET) | يحدد أن المستند المحدد تم ربطه بجدول بيانات Excel عبر نظام تبادل البيانات الديناميكي (DDE). |
| [TEXT_FILE](#TEXT-FILE) | يحدد أن المستند المحدد تم ربطه بملف نصي عبر نظام تبادل البيانات الديناميكي (DDE). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


يحدد أن المستند المحدد تم ربطه بقاعدة بيانات Access عبر نظام تبادل البيانات الديناميكي (DDE).

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يساوي [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي عبر واجهة كائن مصدر بيانات المكتب (ODSO).

### NONE {#NONE}
```
public static int NONE
```


لم يتم تحديد مصدر بيانات دمج البريد.

### ODBC {#ODBC}
```
public static int ODBC
```


يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي عبر واجهة Open Database Connectivity.

### QUERY {#QUERY}
```
public static int QUERY
```


يحدد أن المستند المحدد تم ربطه بمصدر بيانات خارجي باستخدام أداة استعلام خارجية.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


يحدد أن المستند المحدد تم ربطه بجدول بيانات Excel عبر نظام تبادل البيانات الديناميكي (DDE).

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


يحدد أن المستند المحدد تم ربطه بملف نصي عبر نظام تبادل البيانات الديناميكي (DDE).

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDataType) {#toString-int}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
