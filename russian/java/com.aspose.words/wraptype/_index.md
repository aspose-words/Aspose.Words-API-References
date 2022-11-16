---
title: WrapType
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как текст обтекает фигуру или изображение.
type: docs
weight: 622
url: /ru/java/com.aspose.words/wraptype/
---

**Наследование:**
java.lang.Object
```
public class WrapType
```

Указывает, как текст обтекает фигуру или изображение.
## Поля

| Поле | Описание |
| --- | --- |
| [INLINE](#INLINE) | Фигура остается на том же слое, что и текст, и рассматривается как символ. |
| [NONE](#NONE) | Текст не обтекает фигуру. |
| [SQUARE](#SQUARE) | Оборачивает текст вокруг всех сторон квадратной ограничивающей рамки фигуры. |
| [THROUGH](#THROUGH) | То же, что и Tight, но охватывает все открытые части фигуры. |
| [TIGHT](#TIGHT) | Плотно обтекает края фигуры, а не ограничивающую рамку. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Текст останавливается в верхней части фигуры и возобновляется в строке под фигурой. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String wrapTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int wrapType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int wrapType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


Фигура остается на том же слое, что и текст, и рассматривается как символ.

### NONE {#NONE}
```
public static int NONE
```


Текст не обтекает фигуру. Фигура размещается позади или перед текстом.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Оборачивает текст вокруг всех сторон квадратной ограничивающей рамки фигуры.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


То же, что и Tight, но охватывает все открытые части фигуры.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Плотно обтекает края фигуры, а не ограничивающую рамку.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Текст останавливается в верхней части фигуры и возобновляется в строке под фигурой.

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
### fromName(String wrapTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String wrapTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int wrapType) {#getName-int-}
```
public static String getName(int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapType | int |  |

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
### toString(int wrapType) {#toString-int-}
```
public static String toString(int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapType | int |  |

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
