---
title: ViewOptions
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет различные параметры, управляющие отображением документа в Microsoft Word.
type: docs
weight: 601
url: /ru/java/com.aspose.words/viewoptions/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

Предоставляет различные параметры, управляющие отображением документа в Microsoft Word.

 Чтобы узнать больше, посетите**Work with Options and Appearance of Word Documents** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape--) | Управляет отображением формы фона в представлении макета печати. |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries--) | Отключает отображение пространства между верхней частью текста и верхним краем страницы. |
| [getFormsDesign()](#getFormsDesign--) | Указывает, находится ли документ в режиме разработки форм. |
| [getViewType()](#getViewType--) | Управляет режимом просмотра в Microsoft Word. |
| [getZoomPercent()](#getZoomPercent--) | Получает процент (от 10 до 500), при котором вы хотите просмотреть документ. |
| [getZoomType()](#getZoomType--) | Получает значение масштабирования в зависимости от размера окна. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean-) | Управляет отображением формы фона в представлении макета печати. |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean-) | Отключает отображение пространства между верхней частью текста и верхним краем страницы. |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean-) | Указывает, находится ли документ в режиме разработки форм. |
| [setViewType(int value)](#setViewType-int-) | Управляет режимом просмотра в Microsoft Word. |
| [setZoomPercent(int value)](#setZoomPercent-int-) | Устанавливает процент (от 10 до 500), при котором вы хотите просмотреть документ. |
| [setZoomType(int value)](#setZoomType-int-) | Устанавливает значение масштабирования в зависимости от размера окна. |
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
### getDisplayBackgroundShape() {#getDisplayBackgroundShape--}
```
public boolean getDisplayBackgroundShape()
```


Управляет отображением формы фона в представлении макета печати.

**Возвращает:**
boolean - соответствующее логическое значение.
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries--}
```
public boolean getDoNotDisplayPageBoundaries()
```


Отключает отображение пространства между верхней частью текста и верхним краем страницы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFormsDesign() {#getFormsDesign--}
```
public boolean getFormsDesign()
```


Указывает, находится ли документ в режиме разработки форм.

В настоящее время работает только для документов в формате WordML.

**Возвращает:**
boolean - соответствующее логическое значение.
### getViewType() {#getViewType--}
```
public int getViewType()
```


Управляет режимом просмотра в Microsoft Word.

Хотя Aspose.Words может читать и записывать эту опцию, ее использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ViewType](../../com.aspose.words/viewtype) константы.
### getZoomPercent() {#getZoomPercent--}
```
public int getZoomPercent()
```


Получает процент (от 10 до 500), при котором вы хотите просмотреть документ.

Если значение равно 0, то это свойство вместо этого использует 100, иначе, если значение меньше 10 или больше 500, это свойство выдает.

Хотя Aspose.Words может читать и записывать эту опцию, ее использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

**Возвращает:**
int — процент (от 10 до 500), с которым вы хотите просмотреть документ.
### getZoomType() {#getZoomType--}
```
public int getZoomType()
```


Получает значение масштабирования в зависимости от размера окна.

**Возвращает:**
int — значение масштабирования, основанное на размере окна. Возвращаемое значение является одним из[ZoomType](../../com.aspose.words/zoomtype) константы.
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




### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean-}
```
public void setDisplayBackgroundShape(boolean value)
```


Управляет отображением формы фона в представлении макета печати.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean-}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


Отключает отображение пространства между верхней частью текста и верхним краем страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFormsDesign(boolean value) {#setFormsDesign-boolean-}
```
public void setFormsDesign(boolean value)
```


Указывает, находится ли документ в режиме разработки форм.

В настоящее время работает только для документов в формате WordML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setViewType(int value) {#setViewType-int-}
```
public void setViewType(int value)
```


Управляет режимом просмотра в Microsoft Word.

Хотя Aspose.Words может читать и записывать эту опцию, ее использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ViewType](../../com.aspose.words/viewtype) константы. |

### setZoomPercent(int value) {#setZoomPercent-int-}
```
public void setZoomPercent(int value)
```


Устанавливает процент (от 10 до 500), при котором вы хотите просмотреть документ.

Если значение равно 0, то это свойство вместо этого использует 100, иначе, если значение меньше 10 или больше 500, это свойство выдает.

Хотя Aspose.Words может читать и записывать эту опцию, ее использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Процент (от 10 до 500), с которым вы хотите просмотреть документ. |

### setZoomType(int value) {#setZoomType-int-}
```
public void setZoomType(int value)
```


Устанавливает значение масштабирования в зависимости от размера окна.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение масштабирования, основанное на размере окна. Значение должно быть одним из[ZoomType](../../com.aspose.words/zoomtype) константы. |

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
