---
title: ImageType
second_title: Справочник по API Aspose.Words для Java
description: Задает формат типа изображения в документе Microsoft Word.
type: docs
weight: 343
url: /ru/java/com.aspose.words/imagetype/
---

**Наследование:**
java.lang.Object
```
public class ImageType
```

Указывает тип (формат) изображения в документе Microsoft Word.
## Поля

| Поле | Описание |
| --- | --- |
| [BMP](#BMP) | Растровое изображение Windows. |
| [EMF](#EMF) | Расширенный метафайл Windows. |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Нет данных изображения. |
| [PICT](#PICT) | Макинтош ИЗОБРАЖЕНИЕ. |
| [PNG](#PNG) | Портативная сетевая графика. |
| [UNKNOWN](#UNKNOWN) | Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word. |
| [WMF](#WMF) | Метафайл Windows. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String imageTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int imageType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int imageType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BMP {#BMP}
```
public static int BMP
```


Растровое изображение Windows.

### EMF {#EMF}
```
public static int EMF
```


Расширенный метафайл Windows.

### JPEG {#JPEG}
```
public static int JPEG
```


JPEG JFIF.

### NO_IMAGE {#NO-IMAGE}
```
public static int NO_IMAGE
```


Нет данных изображения.

### PICT {#PICT}
```
public static int PICT
```


Макинтош ИЗОБРАЖЕНИЕ. Существующее изображение будет сохранено в документе, но вставка новых изображений PICT в документ не поддерживается.

### PNG {#PNG}
```
public static int PNG
```


Портативная сетевая графика.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word.

### WMF {#WMF}
```
public static int WMF
```


Метафайл Windows.

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
### fromName(String imageTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String imageTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int imageType) {#getName-int-}
```
public static String getName(int imageType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageType | int |  |

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
### toString(int imageType) {#toString-int-}
```
public static String toString(int imageType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageType | int |  |

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
