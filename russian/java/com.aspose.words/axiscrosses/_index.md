---
title: AxisCrosses
second_title: Справочник по API Aspose.Words для Java
description: Определяет возможные точки пересечения оси.
type: docs
weight: 19
url: /ru/java/com.aspose.words/axiscrosses/
---

**Наследование:**
java.lang.Object
```
public class AxisCrosses
```

Определяет возможные точки пересечения оси.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | Ось категорий пересекается в нулевой точке оси значений (если возможно), или в минимальном значении, если минимум больше нуля, или в максимуме, если максимум меньше нуля. |
| [CUSTOM](#CUSTOM) | Перпендикулярная ось пересекает указанное значение оси. |
| [MAXIMUM](#MAXIMUM) | Перпендикулярная ось пересекается при максимальном значении оси. |
| [MINIMUM](#MINIMUM) | Перпендикулярная ось пересекается при минимальном значении оси. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String axisCrossesName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int axisCrosses)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int axisCrosses)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


Ось категорий пересекается в нулевой точке оси значений (если возможно), или в минимальном значении, если минимум больше нуля, или в максимуме, если максимум меньше нуля.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Перпендикулярная ось пересекает указанное значение оси.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Перпендикулярная ось пересекается при максимальном значении оси.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Перпендикулярная ось пересекается при минимальном значении оси.

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
### fromName(String axisCrossesName) {#fromName-java.lang.String-}
```
public static int fromName(String axisCrossesName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| axisCrossesName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int axisCrosses) {#getName-int-}
```
public static String getName(int axisCrosses)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| axisCrosses | int |  |

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
### toString(int axisCrosses) {#toString-int-}
```
public static String toString(int axisCrosses)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| axisCrosses | int |  |

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
