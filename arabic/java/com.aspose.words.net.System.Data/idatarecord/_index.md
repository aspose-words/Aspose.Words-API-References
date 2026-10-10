---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى قيم الأعمدة داخل كل صف لـ DataReader ويتم تنفيذها بواسطة موفري بيانات .NET Framework الذين يصلون إلى قواعد البيانات العلائقية في جافا."
type: docs
weight: 35
url: /ar/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

يوفر وصولًا إلى قيم الأعمدة داخل كل صف لـ DataReader، ويتم تنفيذها بواسطة موفري بيانات .NET Framework الذين يصلون إلى قواعد البيانات العلائقية.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [get(int i)](#get-int) | يحصل على العمود الموجود في الفهرس المحدد. |
| [getFieldCount()](#getFieldCount) | يحصل على عدد الأعمدة في الصف الحالي. |
| [getFieldType(int i)](#getFieldType-int) | يحصل على معلومات java.lang.Class المقابلة لنوع java.lang.Object الذي سيتم إرجاعه من [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | يحصل على الاسم الخاص بالحقل للبحث عنه. |
| [getValue(int i)](#getValue-int) | إرجاع قيمة الحقل المحدد. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


يحصل على العمود الموجود في الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| i | int | الفهرس الصفري للعمود المراد الحصول عليه. |

**Returns:**
java.lang.Object - العمود الموجود في الفهرس المحدد كـ java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


يحصل على عدد الأعمدة في الصف الحالي.

**Returns:**
int - عندما لا يكون في مجموعة سجلات صالحة، 0؛ وإلا، عدد الأعمدة في السجل الحالي. القيمة الافتراضية هي -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


يحصل على معلومات java.lang.Class المقابلة لنوع java.lang.Object الذي سيتم إرجاعه من [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| i | int | فهرس الحقل للبحث عنه. |

**Returns:**
java.lang.Class - معلومات java.lang.Class المقابلة لنوع java.lang.Object الذي سيتم إرجاعه من [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


يحصل على الاسم الخاص بالحقل للبحث عنه.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| i | int | فهرس الحقل للبحث عنه. |

**Returns:**
java.lang.String - اسم الحقل أو السلسلة الفارغة (\"\"), إذا لم توجد قيمة للإرجاع.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


إرجاع قيمة الحقل المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| i | int | فهرس الحقل للبحث عنه. |

**Returns:**
java.lang.Object - الـ java.lang.Object الذي سيحتوي على قيمة الحقل عند الإرجاع.
