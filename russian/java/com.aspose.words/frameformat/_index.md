---
title: FrameFormat
second_title: Справочник по API Aspose.Words для Java
description: Представляет форматирование абзаца, связанное с фреймом.
type: docs
weight: 301
url: /ru/java/com.aspose.words/frameformat/
---

**Наследование:**
java.lang.Object
```
public class FrameFormat
```

Представляет форматирование абзаца, связанное с фреймом.

Этот объект создается всегда. Если абзац является фреймом, все свойства будут содержать соответствующие значения, в противном случае для всех свойств будут установлены значения по умолчанию.

 Использовать[isFrame()](../../com.aspose.words/frameformat\#isFrame--) чтобы проверить, является ли абзац фреймом.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getHeight()](#getHeight--) | Получает высоту указанного кадра. |
| [getHeightRule()](#getHeightRule--) | Получает правило определения высоты указанного фрейма. |
| [getHorizontalAlignment()](#getHorizontalAlignment--) | Получает горизонтальное выравнивание указанного кадра. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText--) | Получает горизонтальное расстояние между фреймом и окружающим текстом в пунктах. |
| [getHorizontalPosition()](#getHorizontalPosition--) |  Получает расстояние по горизонтали между краем фрейма и элементом, указанным[getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) имущество. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition--) | Получает относительное горизонтальное положение фрейма. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition--) | Получает относительное вертикальное положение кадра. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Получает вертикальное выравнивание указанного кадра. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText--) | Указывает расстояние по вертикали (в пунктах) между фреймом и окружающим текстом. |
| [getVerticalPosition()](#getVerticalPosition--) |  Получает расстояние по вертикали между краем фрейма и элементом, указанным[getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) имущество. |
| [getWidth()](#getWidth--) | Получает ширину указанного фрейма в пунктах. |
| [hashCode()](#hashCode--) |  |
| [isFrame()](#isFrame--) | Возвращает true, если абзац является фреймом. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### getHeight() {#getHeight--}
```
public double getHeight()
```


Получает высоту указанного кадра.

**Возвращает:**
double - Высота указанного кадра.
### getHeightRule() {#getHeightRule--}
```
public int getHeightRule()
```


Получает правило определения высоты указанного фрейма.

**Возвращает:**
 int - Правило определения высоты указанного фрейма. Возвращаемое значение является одним из[HeightRule](../../com.aspose.words/heightrule) константы.
### getHorizontalAlignment() {#getHorizontalAlignment--}
```
public int getHorizontalAlignment()
```


Получает горизонтальное выравнивание указанного кадра.

**Возвращает:**
 int - Горизонтальное выравнивание указанного кадра. Возвращаемое значение является одним из[HorizontalAlignment](../../com.aspose.words/horizontalalignment) константы.
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText--}
```
public double getHorizontalDistanceFromText()
```


Получает горизонтальное расстояние между фреймом и окружающим текстом в пунктах.

**Возвращает:**
double - Расстояние по горизонтали между фреймом и окружающим текстом в пунктах.
### getHorizontalPosition() {#getHorizontalPosition--}
```
public double getHorizontalPosition()
```


 Получает расстояние по горизонтали между краем фрейма и элементом, указанным[getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) имущество.

**Возвращает:**
 double - Горизонтальное расстояние между краем рамки и элементом, указанным[getRelativeHorizontalPosition()](../../com.aspose.words/frameformat\#getRelativeHorizontalPosition--) имущество.
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition--}
```
public int getRelativeHorizontalPosition()
```


Получает относительное горизонтальное положение фрейма.

**Возвращает:**
 int - относительное горизонтальное положение кадра. Возвращаемое значение является одним из[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) константы.
### getRelativeVerticalPosition() {#getRelativeVerticalPosition--}
```
public int getRelativeVerticalPosition()
```


Получает относительное вертикальное положение кадра.

**Возвращает:**
 int - относительное вертикальное положение кадра. Возвращаемое значение является одним из[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) константы.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Получает вертикальное выравнивание указанного кадра.

**Возвращает:**
 int - Вертикальное выравнивание указанного кадра. Возвращаемое значение является одним из[VerticalAlignment](../../com.aspose.words/verticalalignment) константы.
### getVerticalDistanceFromText() {#getVerticalDistanceFromText--}
```
public double getVerticalDistanceFromText()
```


Указывает расстояние по вертикали (в пунктах) между фреймом и окружающим текстом.

**Возвращает:**
double - соответствующее двойное значение.
### getVerticalPosition() {#getVerticalPosition--}
```
public double getVerticalPosition()
```


 Получает расстояние по вертикали между краем фрейма и элементом, указанным[getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) имущество.

**Возвращает:**
 double - Расстояние по вертикали между краем рамки и элементом, указанным[getRelativeVerticalPosition()](../../com.aspose.words/frameformat\#getRelativeVerticalPosition--) имущество.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Получает ширину указанного фрейма в пунктах.

**Возвращает:**
double - Ширина указанного фрейма в пунктах.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isFrame() {#isFrame--}
```
public boolean isFrame()
```


Возвращает true, если абзац является фреймом.

**Возвращает:**
boolean — Истинно, если абзац является фреймом.
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
