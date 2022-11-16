---
title: WrapSide
second_title: Справочник по API Aspose.Words для Java
description: Указывает, какие стороны фигуры или изображения обтекает текст.
type: docs
weight: 621
url: /ru/java/com.aspose.words/wrapside/
---

**Наследование:**
java.lang.Object
```
public class WrapSide
```

Указывает, какую сторону (стороны) фигуры или изображения обтекает текст.
## Поля

| Поле | Описание |
| --- | --- |
| [BOTH](#BOTH) | Текст документа обтекает фигуру с обеих сторон. |
| [DEFAULT](#DEFAULT) |  Значение по умолчанию[BOTH](../../com.aspose.words/wrapside\#BOTH). |
| [LARGEST](#LARGEST) | Текст документа обтекает ту сторону фигуры, которая находится дальше всего от полей страницы, оставляя свободную от текста область на другой стороне фигуры. |
| [LEFT](#LEFT) | Текст документа обтекает только левую сторону фигуры. |
| [RIGHT](#RIGHT) | Текст документа обтекает только правую часть фигуры. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String wrapSideName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int wrapSide)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int wrapSide)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BOTH {#BOTH}
```
public static int BOTH
```


Текст документа обтекает фигуру с обеих сторон.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


 Значение по умолчанию[BOTH](../../com.aspose.words/wrapside\#BOTH).

### LARGEST {#LARGEST}
```
public static int LARGEST
```


Текст документа обтекает ту сторону фигуры, которая находится дальше всего от полей страницы, оставляя свободную от текста область на другой стороне фигуры.

### LEFT {#LEFT}
```
public static int LEFT
```


Текст документа обтекает только левую сторону фигуры. Справа от фигуры есть свободная от текста область.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Текст документа обтекает только правую часть фигуры. В левой части фигуры есть свободная от текста область.

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
### fromName(String wrapSideName) {#fromName-java.lang.String-}
```
public static int fromName(String wrapSideName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapSideName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int wrapSide) {#getName-int-}
```
public static String getName(int wrapSide)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapSide | int |  |

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
### toString(int wrapSide) {#toString-int-}
```
public static String toString(int wrapSide)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| wrapSide | int |  |

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
