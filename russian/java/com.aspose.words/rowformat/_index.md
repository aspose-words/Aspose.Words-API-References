---
title: RowFormat
second_title: Справочник по API Aspose.Words для Java
description: Представляет все форматирование строки таблицы.
type: docs
weight: 494
url: /ru/java/com.aspose.words/rowformat/
---

**Наследование:**
java.lang.Object
```
public class RowFormat
```

Представляет все форматирование строки таблицы.

 Чтобы узнать больше, посетите**Working with Tables** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Восстанавливает форматирование строки по умолчанию. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages--) | Значение true, если текст в строке таблицы может разделяться на разрыв страницы. |
| [getBorders()](#getBorders--) | Получает коллекцию границ ячеек по умолчанию для строки. |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getHeadingFormat()](#getHeadingFormat--) | Истинно, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы. |
| [getHeight()](#getHeight--) | Получает высоту строки таблицы в пунктах. |
| [getHeightRule()](#getHeightRule--) | Получает правило определения высоты строки таблицы. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean-) | Значение true, если текст в строке таблицы может разделяться на разрыв страницы. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setHeadingFormat(boolean value)](#setHeadingFormat-boolean-) | Истинно, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы. |
| [setHeight(double value)](#setHeight-double-) | Устанавливает высоту строки таблицы в пунктах. |
| [setHeightRule(int value)](#setHeightRule-int-) | Задает правило определения высоты строки таблицы. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Восстанавливает форматирование строки по умолчанию.

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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages--}
```
public boolean getAllowBreakAcrossPages()
```


Значение true, если текст в строке таблицы может разделяться на разрыв страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ ячеек по умолчанию для строки.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ ячеек по умолчанию для строки.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getHeadingFormat() {#getHeadingFormat--}
```
public boolean getHeadingFormat()
```


Истинно, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getHeight() {#getHeight--}
```
public double getHeight()
```


Получает высоту строки таблицы в пунктах.

**Возвращает:**
double - Высота строки таблицы в пунктах.
### getHeightRule() {#getHeightRule--}
```
public int getHeightRule()
```


Получает правило определения высоты строки таблицы.

**Возвращает:**
 int - Правило определения высоты строки таблицы. Возвращаемое значение является одним из[HeightRule](../../com.aspose.words/heightrule) константы.
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




### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean-}
```
public void setAllowBreakAcrossPages(boolean value)
```


Значение true, если текст в строке таблицы может разделяться на разрыв страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setHeadingFormat(boolean value) {#setHeadingFormat-boolean-}
```
public void setHeadingFormat(boolean value)
```


Истинно, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


Устанавливает высоту строки таблицы в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Высота строки таблицы в пунктах. |

### setHeightRule(int value) {#setHeightRule-int-}
```
public void setHeightRule(int value)
```


Задает правило определения высоты строки таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Правило определения высоты строки таблицы. Значение должно быть одним из[HeightRule](../../com.aspose.words/heightrule) константы. |

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
