---
title: "Правило"
linktitle: "Правило"
second_title: "Aspose.Words для Java"
description: "Указывает действие, которое происходит, когда в Java применяется ForeignKeyConstraint."
type: docs
weight: 36
url: /ru/java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

Указывает действие, которое происходит, когда применяется [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
## Поля

| Поле | Описание |
| --- | --- |
| [CASCADE](#CASCADE) | Удалить или обновить связанные строки. |
| [NONE](#NONE) | Для связанных строк не предпринимается никаких действий. |
| [SET_DEFAULT](#SET-DEFAULT) | Установить значения в связанных строках в значение, содержащееся в свойстве [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object). |
| [SET_NULL](#SET-NULL) | Установить значения в связанных строках в DBNull. |
## Методы

| Метод | Описание |
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


Удалить или обновить связанные строки. Это значение по умолчанию.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


Для связанных строк не предпринимается никаких действий.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Установить значения в связанных строках в значение, содержащееся в свойстве [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object).

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Установить значения в связанных строках в DBNull.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
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
