---
title: AxisScaling
second_title: Справочник по API Aspose.Words для Java
description: Представляет параметры масштабирования оси.
type: docs
weight: 22
url: /ru/java/com.aspose.words/axisscaling/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class AxisScaling implements Cloneable
```

Представляет параметры масштабирования оси.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getLogBase()](#getLogBase--) | Получает основание логарифма для логарифмической оси. |
| [getMaximum()](#getMaximum--) | Получает максимальное значение оси. |
| [getMinimum()](#getMinimum--) | Получает минимальное значение оси. |
| [getType()](#getType--) | Получает тип масштабирования оси. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setLogBase(double value)](#setLogBase-double-) | Устанавливает основание логарифма для логарифмической оси. |
| [setMaximum(AxisBound value)](#setMaximum-com.aspose.words.AxisBound-) | Устанавливает максимальное значение оси. |
| [setMinimum(AxisBound value)](#setMinimum-com.aspose.words.AxisBound-) | Устанавливает минимальное значение оси. |
| [setType(int value)](#setType-int-) | Задает тип масштабирования оси. |
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
### getLogBase() {#getLogBase--}
```
public double getLogBase()
```


Получает основание логарифма для логарифмической оси.

Это свойство не поддерживается новыми диаграммами MS Office 2016.

 Допустимый диапазон значений с плавающей запятой больше или равен 2 и меньше или равен 1000. Свойство действует, только если[getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) установлен на[AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

 Установка этого свойства устанавливает[getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) собственность на[AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**Возвращает:**
double - Логарифмическое основание для логарифмической оси.
### getMaximum() {#getMaximum--}
```
public AxisBound getMaximum()
```


Получает максимальное значение оси. Значение по умолчанию — «авто».

**Возвращает:**
[AxisBound](../../com.aspose.words/axisbound) - Максимальное значение оси.
### getMinimum() {#getMinimum--}
```
public AxisBound getMinimum()
```


Получает минимальное значение оси. Значение по умолчанию — «авто».

**Возвращает:**
[AxisBound](../../com.aspose.words/axisbound) - Минимальное значение оси.
### getType() {#getType--}
```
public int getType()
```


 Получает тип масштабирования оси.[AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR) значение — единственное, что разрешено в новых диаграммах MS Office 2016.

**Возвращает:**
 int - Тип масштабирования оси. Возвращаемое значение является одним из[AxisScaleType](../../com.aspose.words/axisscaletype) константы.
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




### setLogBase(double value) {#setLogBase-double-}
```
public void setLogBase(double value)
```


Устанавливает основание логарифма для логарифмической оси.

Это свойство не поддерживается новыми диаграммами MS Office 2016.

 Допустимый диапазон значений с плавающей запятой больше или равен 2 и меньше или равен 1000. Свойство действует, только если[getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) установлен на[AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

 Установка этого свойства устанавливает[getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) собственность на[AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Логарифмическое основание для логарифмической оси. |

### setMaximum(AxisBound value) {#setMaximum-com.aspose.words.AxisBound-}
```
public void setMaximum(AxisBound value)
```


Устанавливает максимальное значение оси. Значение по умолчанию — «авто».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | Максимальное значение оси. |

### setMinimum(AxisBound value) {#setMinimum-com.aspose.words.AxisBound-}
```
public void setMinimum(AxisBound value)
```


Устанавливает минимальное значение оси. Значение по умолчанию — «авто».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | Минимальное значение оси. |

### setType(int value) {#setType-int-}
```
public void setType(int value)
```


 Задает тип масштабирования оси.[AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR) значение — единственное, что разрешено в новых диаграммах MS Office 2016.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип масштабирования оси. Значение должно быть одним из[AxisScaleType](../../com.aspose.words/axisscaletype) константы. |

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
