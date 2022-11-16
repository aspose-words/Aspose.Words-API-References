---
title: Rule
second_title: Справочник по API Aspose.Words для Java
description: Указывает действие, которое происходит при принудительном применении a.
type: docs
weight: 36
url: /ru/java/com.aspose.words.net.system.data/rule/
---

**Наследование:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

 Указывает действие, которое происходит, когда[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint) применяется.
## Поля

| Поле | Описание |
| --- | --- |
| [CASCADE](#CASCADE) | Удалить или обновить связанные строки. |
| [NONE](#NONE) | Никаких действий со связанными строками не предпринимается. |
| [SET_DEFAULT](#SET-DEFAULT) | Установите значения в связанных строках на значение, содержащееся в[DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-) имущество. |
| [SET_NULL](#SET-NULL) | Установите значения в связанных строках в DBNull. |
## Методы

| Метод | Описание |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String-) |  |
| [compareTo(E arg0)](#compareTo-E-) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDeclaringClass()](#getDeclaringClass--) |  |
| [hashCode()](#hashCode--) |  |
| [name()](#name--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [ordinal()](#ordinal--) |  |
| [toString()](#toString--) |  |
| [valueOf(String name)](#valueOf-java.lang.String-) |  |
| [values()](#values--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


Удалить или обновить связанные строки. Это значение по умолчанию.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


Никаких действий со связанными строками не предпринимается.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Установите значения в связанных строках на значение, содержащееся в[DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn\#getDefaultValue--) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn\#setDefaultValue-java.lang.Object-) имущество.

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Установите значения в связанных строках в DBNull.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String-}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Возвращает:**
Т
### compareTo(E arg0) {#compareTo-E-}
```
public final int compareTo(E arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | E |  |

**Возвращает:**
инт
### equals(Object arg0) {#equals-java.lang.Object-}
```
public final boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDeclaringClass() {#getDeclaringClass--}
```
public final Class<E> getDeclaringClass()
```




**Возвращает:**
java.lang.Класс<E>
### hashCode() {#hashCode--}
```
public final int hashCode()
```




**Возвращает:**
инт
### name() {#name--}
```
public final String name()
```




**Возвращает:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### ordinal() {#ordinal--}
```
public final int ordinal()
```




**Возвращает:**
инт
### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String-}
```
public static System.Data.Rule valueOf(String name)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |

**Возвращает:**
[Rule](../../com.aspose.words.net.system.data/rule)
### values() {#values--}
```
public static System.Data.Rule[] values()
```




**Возвращает:**
com.aspose.words.net.System.Data.Rule[]
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
