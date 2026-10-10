---
title: "قاعدة"
linktitle: "قاعدة"
second_title: "Aspose.Words لـ Java"
description: "يشير إلى الإجراء الذي يحدث عندما يتم تطبيق ForeignKeyConstraint في Java."
type: docs
weight: 36
url: /ar/java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

يشير إلى الإجراء الذي يحدث عندما يتم تطبيق [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
## الحقول

| حقل | الوصف |
| --- | --- |
| [CASCADE](#CASCADE) | حذف أو تحديث الصفوف المرتبطة. |
| [NONE](#NONE) | لم يتم اتخاذ أي إجراء على الصفوف المرتبطة. |
| [SET_DEFAULT](#SET-DEFAULT) | تعيين القيم في الصفوف المرتبطة إلى القيمة الموجودة في الخاصية [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object). |
| [SET_NULL](#SET-NULL) | تعيين القيم في الصفوف المرتبطة إلى DBNull. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


حذف أو تحديث الصفوف المرتبطة. هذا هو الإعداد الافتراضي.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


لم يتم اتخاذ أي إجراء على الصفوف المرتبطة.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


تعيين القيم في الصفوف المرتبطة إلى القيمة الموجودة في الخاصية [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object).

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


تعيين القيم في الصفوف المرتبطة إلى DBNull.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.Rule valueOf(String name)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/)
### values() {#values}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
