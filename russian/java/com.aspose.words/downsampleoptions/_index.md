---
title: DownsampleOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать параметры понижающей дискретизации.
type: docs
weight: 133
url: /ru/java/com.aspose.words/downsampleoptions/
---

**Наследование:**
java.lang.Object
```
public class DownsampleOptions
```

Позволяет указать параметры понижающей дискретизации.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDownsampleImages()](#getDownsampleImages--) | Указывает, следует ли уменьшать разрешение изображений. |
| [getResolution()](#getResolution--) | Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены. |
| [getResolutionThreshold()](#getResolutionThreshold--) | Указывает пороговое разрешение в пикселях на дюйм. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDownsampleImages(boolean value)](#setDownsampleImages-boolean-) | Указывает, следует ли уменьшать разрешение изображений. |
| [setResolution(int value)](#setResolution-int-) | Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены. |
| [setResolutionThreshold(int value)](#setResolutionThreshold-int-) | Указывает пороговое разрешение в пикселях на дюйм. |
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
### getDownsampleImages() {#getDownsampleImages--}
```
public boolean getDownsampleImages()
```


Указывает, следует ли уменьшать разрешение изображений. Значение по умолчанию верно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getResolution() {#getResolution--}
```
public int getResolution()
```


Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены. Значение по умолчанию — 220 пикселей на дюйм.

**Возвращает:**
int - соответствующее значение int.
### getResolutionThreshold() {#getResolutionThreshold--}
```
public int getResolutionThreshold()
```


Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения разрешения применяться не будет. Значение 0 означает, что проверка порога не используется, и все изображения, размер которых можно уменьшить, уменьшаются. Значение по умолчанию — 0.

**Возвращает:**
int - соответствующее значение int.
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




### setDownsampleImages(boolean value) {#setDownsampleImages-boolean-}
```
public void setDownsampleImages(boolean value)
```


Указывает, следует ли уменьшать разрешение изображений. Значение по умолчанию верно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setResolution(int value) {#setResolution-int-}
```
public void setResolution(int value)
```


Указывает разрешение в пикселях на дюйм, до которого изображения должны быть уменьшены. Значение по умолчанию — 220 пикселей на дюйм.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setResolutionThreshold(int value) {#setResolutionThreshold-int-}
```
public void setResolutionThreshold(int value)
```


Указывает пороговое разрешение в пикселях на дюйм. Если разрешение изображения в документе меньше порогового значения, алгоритм понижения разрешения применяться не будет. Значение 0 означает, что проверка порога не используется, и все изображения, размер которых можно уменьшить, уменьшаются. Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

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
