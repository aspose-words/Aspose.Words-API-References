---
title: ConvertUtil
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет вспомогательные функции для преобразования между различными единицами измерения.
type: docs
weight: 95
url: /ru/java/com.aspose.words/convertutil/
---

**Наследование:**
java.lang.Object
```
public class ConvertUtil
```

Предоставляет вспомогательные функции для преобразования между различными единицами измерения.

 Чтобы узнать больше, посетите**Convert Between Measurement Units** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [inchToPoint(double inches)](#inchToPoint-double-) | Преобразует дюймы в пункты. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double-) | Преобразует миллиметры в точки. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double-) | Преобразует пиксели из одного разрешения в другое. |
| [pixelToPoint(double pixels)](#pixelToPoint-double-) | Преобразует пиксели в точки. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double-) | Преобразует пиксели в точки с указанным разрешением в пикселях. |
| [pointToInch(double points)](#pointToInch-double-) | Преобразует пункты в дюймы. |
| [pointToPixel(double points)](#pointToPixel-double-) | Преобразует точки в пиксели. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double-) | Преобразует точки в пиксели с указанным разрешением в пикселях. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### inchToPoint(double inches) {#inchToPoint-double-}
```
public static double inchToPoint(double inches)
```


Преобразует дюймы в пункты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| inches | double | Значение для преобразования. 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### millimeterToPoint(double millimeters) {#millimeterToPoint-double-}
```
public static double millimeterToPoint(double millimeters)
```


Преобразует миллиметры в точки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| millimeters | double | Значение для преобразования. 1 дюйм равен 25,4 миллиметра. 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double-}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Преобразует пиксели из одного разрешения в другое.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pixels | double | Значение для преобразования. |
| oldDpi | double | Текущее разрешение dpi (точек на дюйм). |
| newDpi | double | Новое разрешение dpi (точек на дюйм). |

**Возвращает:**
инт
### pixelToPoint(double pixels) {#pixelToPoint-double-}
```
public static double pixelToPoint(double pixels)
```


Преобразует пиксели в точки. Преобразует пиксели в точки с разрешением 96 dpi.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pixels | double | Значение для преобразования. 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double-}
```
public static double pixelToPoint(double pixels, double resolution)
```


Преобразует пиксели в точки с указанным разрешением в пикселях.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pixels | double | Значение для преобразования. |
| resolution | double | Разрешение dpi (точек на дюйм). 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### pointToInch(double points) {#pointToInch-double-}
```
public static double pointToInch(double points)
```


Преобразует пункты в дюймы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | double | Значение для преобразования. 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### pointToPixel(double points) {#pointToPixel-double-}
```
public static double pointToPixel(double points)
```


Преобразует точки в пиксели. Преобразует точки в пиксели с разрешением 96 dpi.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | double | Значение для преобразования. 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### pointToPixel(double points, double resolution) {#pointToPixel-double-double-}
```
public static double pointToPixel(double points, double resolution)
```


Преобразует точки в пиксели с указанным разрешением в пикселях.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| points | double | Значение для преобразования. |
| resolution | double | Разрешение dpi (точек на дюйм). 1 дюйм равен 72 точкам. |

**Возвращает:**
двойной
### toString() {#toString--}
```
public String toString()
```




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
