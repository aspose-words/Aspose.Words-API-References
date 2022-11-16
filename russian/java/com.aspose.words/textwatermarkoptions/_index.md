---
title: TextWatermarkOptions
second_title: Справочник по API Aspose.Words для Java
description: Содержит параметры, которые можно указать при добавлении водяного знака с текстом.
type: docs
weight: 569
url: /ru/java/com.aspose.words/textwatermarkoptions/
---

**Наследование:**
java.lang.Object
```
public class TextWatermarkOptions
```

Содержит параметры, которые можно указать при добавлении водяного знака с текстом.

 Чтобы узнать больше, посетите**Working with Watermark** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Получает цвет шрифта. |
| [getFontFamily()](#getFontFamily--) | Получает имя семейства шрифтов. |
| [getFontSize()](#getFontSize--) | Получает размер шрифта. |
| [getLayout()](#getLayout--) | Получает макет водяного знака. |
| [hashCode()](#hashCode--) |  |
| [isSemitrasparent()](#isSemitrasparent--) | Получает логическое значение, отвечающее за непрозрачность водяного знака. |
| [isSemitrasparent(boolean value)](#isSemitrasparent-boolean-) | Устанавливает логическое значение, отвечающее за непрозрачность водяного знака. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | Устанавливает цвет шрифта. |
| [setFontFamily(String value)](#setFontFamily-java.lang.String-) | Устанавливает имя семейства шрифтов. |
| [setFontSize(float value)](#setFontSize-float-) | Устанавливает размер шрифта. |
| [setLayout(int value)](#setLayout-int-) | Устанавливает макет водяного знака. |
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
### getColor() {#getColor--}
```
public Color getColor()
```


Получает цвет шрифта. Значение по умолчанию — Color.Silver.

**Возвращает:**
java.awt.Color — цвет шрифта.
### getFontFamily() {#getFontFamily--}
```
public String getFontFamily()
```


Получает имя семейства шрифтов. Значение по умолчанию — «Калибри».

**Возвращает:**
java.lang.String — название семейства шрифтов.
### getFontSize() {#getFontSize--}
```
public float getFontSize()
```


Получает размер шрифта. Значение по умолчанию: 0 — автоматически.

Допустимые значения находятся в диапазоне от 0 до 65,5 включительно.

Автоматический размер шрифта означает, что водяной знак будет масштабироваться до максимальной ширины и максимальной высоты относительно полей страницы.

**Возвращает:**
float — размер шрифта.
### getLayout() {#getLayout--}
```
public int getLayout()
```


 Получает макет водяного знака. Значение по умолчанию[WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Возвращает:**
 int — макет водяного знака. Возвращаемое значение является одним из[WatermarkLayout](../../com.aspose.words/watermarklayout) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isSemitrasparent() {#isSemitrasparent--}
```
public boolean isSemitrasparent()
```


Получает логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию верно.

**Возвращает:**
boolean — логическое значение, отвечающее за непрозрачность водяного знака.
### isSemitrasparent(boolean value) {#isSemitrasparent-boolean-}
```
public void isSemitrasparent(boolean value)
```


Устанавливает логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию верно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, отвечающее за непрозрачность водяного знака. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Устанавливает цвет шрифта. Значение по умолчанию — Color.Silver.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет шрифта. |

### setFontFamily(String value) {#setFontFamily-java.lang.String-}
```
public void setFontFamily(String value)
```


Устанавливает имя семейства шрифтов. Значение по умолчанию — «Калибри».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название семейства шрифтов. |

### setFontSize(float value) {#setFontSize-float-}
```
public void setFontSize(float value)
```


Устанавливает размер шрифта. Значение по умолчанию: 0 — автоматически.

Допустимые значения находятся в диапазоне от 0 до 65,5 включительно.

Автоматический размер шрифта означает, что водяной знак будет масштабироваться до максимальной ширины и максимальной высоты относительно полей страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | float | Размер шрифта. |

### setLayout(int value) {#setLayout-int-}
```
public void setLayout(int value)
```


 Устанавливает макет водяного знака. Значение по умолчанию[WatermarkLayout.DIAGONAL](../../com.aspose.words/watermarklayout\#DIAGONAL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Макет водяного знака. Значение должно быть одним из[WatermarkLayout](../../com.aspose.words/watermarklayout) константы. |

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
