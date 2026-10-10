---
title: "Kural"
linktitle: "Kural"
second_title: "Aspose.Words Java için"
description: "Bir ForeignKeyConstraint Java'da uygulandığında gerçekleşen eylemi gösterir."
type: docs
weight: 36
url: /tr/java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

Bir [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) uygulandığında gerçekleşen eylemi gösterir.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CASCADE](#CASCADE) | İlgili satırları sil veya güncelle. |
| [NONE](#NONE) | İlgili satırlarda hiçbir işlem yapılmaz. |
| [SET_DEFAULT](#SET-DEFAULT) | İlgili satırlardaki değerleri, [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object) özelliğinde bulunan değere ayarla. |
| [SET_NULL](#SET-NULL) | İlgili satırlardaki değerleri DBNull'ye ayarla. |
## Yöntemler

| Yöntem | Açıklama |
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


İlgili satırları sil veya güncelle. Bu varsayılandır.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


İlgili satırlarda hiçbir işlem yapılmaz.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


İlgili satırlardaki değerleri, [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object) özelliğinde bulunan değere ayarla.

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


İlgili satırlardaki değerleri DBNull'ye ayarla.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/)
### values() {#values}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
