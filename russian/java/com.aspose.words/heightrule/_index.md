---
title: HeightRule
second_title: Справочник по API Aspose.Words для Java
description: Задает правило определения высоты объекта.
type: docs
weight: 319
url: /ru/java/com.aspose.words/heightrule/
---

**Наследование:**
java.lang.Object
```
public class HeightRule
```

Задает правило определения высоты объекта.
## Поля

| Поле | Описание |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Высота будет не меньше указанной высоты в пунктах. |
| [AUTO](#AUTO) | Высота будет увеличиваться автоматически, чтобы вместить весь текст внутри объекта. |
| [EXACTLY](#EXACTLY) | Высота указана точно в пунктах. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String heightRuleName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int heightRule)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int heightRule)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Высота будет не меньше указанной высоты в пунктах. При необходимости он будет увеличиваться, чтобы вместить весь текст внутри объекта.

### AUTO {#AUTO}
```
public static int AUTO
```


Высота будет увеличиваться автоматически, чтобы вместить весь текст внутри объекта.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Высота указана точно в пунктах. Обратите внимание, что если текст не помещается внутри объекта такой высоты, он будет отображаться обрезанным.

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
### fromName(String heightRuleName) {#fromName-java.lang.String-}
```
public static int fromName(String heightRuleName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int heightRule) {#getName-int-}
```
public static String getName(int heightRule)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRule | int |  |

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
### toString(int heightRule) {#toString-int-}
```
public static String toString(int heightRule)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| heightRule | int |  |

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
