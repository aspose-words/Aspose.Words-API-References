---
title: PreferredWidthType
second_title: Справочник по API Aspose.Words для Java
description: Задает единицу измерения предпочтительной ширины таблицы или ячейки.
type: docs
weight: 467
url: /ru/java/com.aspose.words/preferredwidthtype/
---

**Наследование:**
java.lang.Object
```
public class PreferredWidthType
```

Задает единицу измерения предпочтительной ширины таблицы или ячейки.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Предпочтительная ширина не указана. |
| [PERCENT](#PERCENT) | Измерьте ширину текущего элемента, используя указанный процент. |
| [POINTS](#POINTS) | Измерьте ширину текущего элемента, используя указанное количество точек (1/72 дюйма). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int preferredWidthType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int preferredWidthType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Предпочтительная ширина не указана. Фактическая ширина таблицы или ячейки либо указывается явной шириной, либо определяется автоматически алгоритмом компоновки таблицы при отображении таблицы, в зависимости от настройки автоподбора таблицы.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Измерьте ширину текущего элемента, используя указанный процент.

### POINTS {#POINTS}
```
public static int POINTS
```


Измерьте ширину текущего элемента, используя указанное количество точек (1/72 дюйма).

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
### fromName(String preferredWidthTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String preferredWidthTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int preferredWidthType) {#getName-int-}
```
public static String getName(int preferredWidthType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthType | int |  |

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
### toString(int preferredWidthType) {#toString-int-}
```
public static String toString(int preferredWidthType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| preferredWidthType | int |  |

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
