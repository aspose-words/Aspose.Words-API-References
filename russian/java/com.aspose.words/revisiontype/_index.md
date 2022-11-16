---
title: RevisionType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип отслеживаемых изменений в .
type: docs
weight: 490
url: /ru/java/com.aspose.words/revisiontype/
---

**Наследование:**
java.lang.Object
```
public class RevisionType
```

 Указывает тип отслеживаемого изменения[Revision](../../com.aspose.words/revision).
## Поля

| Поле | Описание |
| --- | --- |
| [DELETION](#DELETION) | Содержимое было удалено из документа. |
| [FORMAT_CHANGE](#FORMAT-CHANGE) | Изменение форматирования было применено к родительскому узлу. |
| [INSERTION](#INSERTION) | В документ было вставлено новое содержимое. |
| [MOVING](#MOVING) | Содержимое документа было перемещено. |
| [STYLE_DEFINITION_CHANGE](#STYLE-DEFINITION-CHANGE) | Изменение форматирования было применено к родительскому стилю. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String revisionTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int revisionType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int revisionType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DELETION {#DELETION}
```
public static int DELETION
```


Содержимое было удалено из документа.

### FORMAT_CHANGE {#FORMAT-CHANGE}
```
public static int FORMAT_CHANGE
```


Изменение форматирования было применено к родительскому узлу.

### INSERTION {#INSERTION}
```
public static int INSERTION
```


В документ было вставлено новое содержимое.

### MOVING {#MOVING}
```
public static int MOVING
```


Содержимое документа было перемещено.

### STYLE_DEFINITION_CHANGE {#STYLE-DEFINITION-CHANGE}
```
public static int STYLE_DEFINITION_CHANGE
```


Изменение форматирования было применено к родительскому стилю.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String revisionTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int revisionType) {#getName-int-}
```
public static String getName(int revisionType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int revisionType) {#toString-int-}
```
public static String toString(int revisionType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| revisionType | int |  |

**Возвращает:**
java.lang.String
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
