---
title: Watermark
second_title: Справочник по API Aspose.Words для Java
description: Представляет класс для работы с водяным знаком документа.
type: docs
weight: 608
url: /ru/java/com.aspose.words/watermark/
---

**Наследование:**
java.lang.Object
```
public class Watermark
```

Представляет класс для работы с водяным знаком документа.

 Чтобы узнать больше, посетите**Working with Watermark** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getType()](#getType--) | Получает тип водяного знака. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет водяной знак. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | Добавляет водяной знак изображения в документ. |
| [setImage(BufferedImage image, ImageWatermarkOptions options)](#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-) | Добавляет водяной знак изображения в документ. |
| [setImage(String imagePath, ImageWatermarkOptions options)](#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-) | Добавляет водяной знак изображения в документ. |
| [setText(String text)](#setText-java.lang.String-) | Добавляет текстовый водяной знак в документ. |
| [setText(String text, TextWatermarkOptions options)](#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-) | Добавляет текстовый водяной знак в документ. |
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
### getType() {#getType--}
```
public int getType()
```


Получает тип водяного знака.

**Возвращает:**
 int — тип водяного знака. Возвращаемое значение является одним из[WatermarkType](../../com.aspose.words/watermarktype) константы.
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




### remove() {#remove--}
```
public void remove()
```


Удаляет водяной знак.

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


Добавляет водяной знак изображения в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Изображение, которое отображается как водяной знак. |

### setImage(BufferedImage image, ImageWatermarkOptions options) {#setImage-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(BufferedImage image, ImageWatermarkOptions options)
```


Добавляет водяной знак изображения в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Изображение, которое отображается как водяной знак. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | Определяет дополнительные параметры водяного знака изображения. |

### setImage(String imagePath, ImageWatermarkOptions options) {#setImage-java.lang.String-com.aspose.words.ImageWatermarkOptions-}
```
public void setImage(String imagePath, ImageWatermarkOptions options)
```


Добавляет водяной знак изображения в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imagePath | java.lang.String | Путь к файлу изображения, которое отображается в виде водяного знака. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions) | Определяет дополнительные параметры водяного знака изображения. |

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


Добавляет текстовый водяной знак в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Текст, отображаемый в виде водяного знака. Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть нулевым или содержать только пробелы. |

### setText(String text, TextWatermarkOptions options) {#setText-java.lang.String-com.aspose.words.TextWatermarkOptions-}
```
public void setText(String text, TextWatermarkOptions options)
```


Добавляет текстовый водяной знак в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Текст, отображаемый в виде водяного знака. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions) | Определяет дополнительные параметры текстового водяного знака. Длина текста должна быть в диапазоне от 1 до 200 включительно. Текст не может быть нулевым или содержать только пробелы. |

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
