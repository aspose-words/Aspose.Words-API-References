---
title: AxisDisplayUnit
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений.
type: docs
weight: 20
url: /ru/java/com.aspose.words/axisdisplayunit/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCustomUnit()](#getCustomUnit--) | Получает определяемый пользователем делитель для масштабирования единиц отображения на оси значений. |
| [getDocument()](#getDocument--) | Возвращает документ, принадлежащий правообладателю. |
| [getTitle()](#getTitle--) |  |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [getUnit()](#getUnit--) | Получает значение масштабирования отображаемых единиц как одно из предопределенных значений. |
| [hashCode()](#hashCode--) |  |
| [isVisible()](#isVisible--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCustomUnit(double value)](#setCustomUnit-double-) | Задает определяемый пользователем делитель для масштабирования единиц отображения на оси значений. |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
| [setUnit(int value)](#setUnit-int-) | Устанавливает значение масштабирования единиц отображения в качестве одного из предопределенных значений. |
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
### getCustomUnit() {#getCustomUnit--}
```
public double getCustomUnit()
```


Получает определяемый пользователем делитель для масштабирования единиц отображения на оси значений.

Это свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию — 1.

 Установка этого свойства устанавливает[getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-) собственность на[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**Возвращает:**
double — определяемый пользователем делитель для масштабирования единиц отображения на оси значений.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Возвращает документ, принадлежащий правообладателю.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, принадлежащий правообладателю.
### getTitle() {#getTitle--}
```
public ChartTitle getTitle()
```




**Возвращает:**
[ChartTitle](../../com.aspose.words/charttitle)
### getTitleDeleted() {#getTitleDeleted--}
```
public boolean getTitleDeleted()
```




**Возвращает:**
логический
### getTitlePosition() {#getTitlePosition--}
```
public int getTitlePosition()
```




**Возвращает:**
инт
### getUnit() {#getUnit--}
```
public int getUnit()
```


 Получает значение масштабирования отображаемых единиц как одно из предопределенных значений. Значение по умолчанию[AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE) .[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM) а также[AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE) значения недоступны в некоторых типах диаграмм; видеть[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) Чтобы получить больше информации.

**Возвращает:**
 int — значение масштабирования единиц отображения как одно из предопределенных значений. Возвращаемое значение является одним из[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isVisible() {#isVisible--}
```
public boolean isVisible()
```




**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCustomUnit(double value) {#setCustomUnit-double-}
```
public void setCustomUnit(double value)
```


Задает определяемый пользователем делитель для масштабирования единиц отображения на оси значений.

Это свойство не поддерживается новыми диаграммами MS Office 2016. Значение по умолчанию — 1.

 Установка этого свойства устанавливает[getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-) собственность на[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Определяемый пользователем делитель для масштабирования единиц отображения на оси значений. |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle-}
```
public void setTitle(ChartTitle value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean-}
```
public void setTitleDeleted(boolean value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


Устанавливает значение масштабирования единиц отображения в качестве одного из предопределенных значений. Значение по умолчанию[AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE) .[AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM) а также[AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE) значения недоступны в некоторых типах диаграмм; видеть[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) Чтобы получить больше информации.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение масштабирования отображаемых единиц как одно из предопределенных значений. Значение должно быть одним из[AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) константы. |

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
