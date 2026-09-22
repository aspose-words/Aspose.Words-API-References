---
title: "MailMergeDestination"
linktitle: "MailMergeDestination"
second_title: "Aspose.Words لـ Java"
description: "يحدد النتائج المحتملة التي قد تُنتج عند إجراء دمج بريد على مستند في Java."
type: docs
weight: 441
url: /ar/java/com.aspose.words/mailmergedestination/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDestination
```

يحدد النتائج الممكنة التي قد تُنتج عند تنفيذ دمج البريد على مستند.
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | يساوي قيمة [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT). |
| [EMAIL](#EMAIL) | يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ رسائل بريد إلكتروني باستخدام المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| [FAX](#FAX) | يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ فاكسات باستخدام المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ مستندات جديدة عن طريق تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد. |
| [PRINTER](#PRINTER) | يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تطبع المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات خارجية من مصدر البيانات الخارجي المحدد. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDestination)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDestination)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يساوي قيمة [NEW\_DOCUMENT](../../com.aspose.words/mailmergedestination/\#NEW-DOCUMENT).

### EMAIL {#EMAIL}
```
public static int EMAIL
```


يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ رسائل بريد إلكتروني باستخدام المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد.

### FAX {#FAX}
```
public static int FAX
```


يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ فاكسات باستخدام المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد.

### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تُنشئ مستندات جديدة عن طريق تعبئة الحقول داخل مستند معين ببيانات من مصدر البيانات الخارجي المحدد.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


يحدد أن التطبيقات المستضيفة المتوافقة يجب أن تطبع المستندات التي تنتج عن تعبئة الحقول داخل مستند معين ببيانات خارجية من مصدر البيانات الخارجي المحدد.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDestinationName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDestinationName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDestination) {#getName-int}
```
public static String getName(int mailMergeDestination)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDestination) {#toString-int}
```
public static String toString(int mailMergeDestination)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
