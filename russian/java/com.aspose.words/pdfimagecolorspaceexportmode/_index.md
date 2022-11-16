---
title: PdfImageColorSpaceExportMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как цветовое пространство будет выбрано для изображений в документе PDF.
type: docs
weight: 456
url: /ru/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Наследование:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Указывает, как цветовое пространство будет выбрано для изображений в документе PDF.
## Поля

| Поле | Описание |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words автоматически выбирает наиболее подходящее цветовое пространство для каждого изображения. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words преобразует изображения RGB в цветовое пространство CMYK, используя простую формулу. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words автоматически выбирает наиболее подходящее цветовое пространство для каждого изображения.

Большинство изображений сохраняются в цветовом пространстве RGB. Также могут использоваться индексированные и оттенки серого цветовые пространства. Цветовое пространство CMYK никогда не используется.

Для некоторых изображений цветовое пространство может отличаться на разных платформах.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words преобразует изображения RGB в цветовое пространство CMYK, используя простую формулу.

Изображения в цветовом пространстве RGB преобразуются в CMYK по формуле: черный = минимум (1-красный, 1-зеленый, 1-синий). Голубой = (1-красный-черный)/(1-черный). Пурпурный = (1-зеленый-черный)/(1-черный). Желтый = (1-синий-черный)/(1-черный). Значения RGB нормализованы — они находятся в диапазоне от 0 до 1,0.

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
### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfImageColorSpaceExportMode) {#getName-int-}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

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
### toString(int pdfImageColorSpaceExportMode) {#toString-int-}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

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
