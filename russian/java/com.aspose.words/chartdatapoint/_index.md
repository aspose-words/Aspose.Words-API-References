---
title: ChartDataPoint
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать форматирование одной точки данных на диаграмме.
type: docs
weight: 60
url: /ru/java/com.aspose.words/chartdatapoint/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartDataPoint implements IChartDataPoint, Cloneable
```

Позволяет указать форматирование одной точки данных на диаграмме.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.

 В сериале,[ChartDataPoint](../../com.aspose.words/chartdatapoint) объект является членом[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) .[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) содержит[ChartDataPoint](../../com.aspose.words/chartdatapoint) объект для каждой точки.
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormat()](#clearFormat--) | Очищает формат этой точки данных. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [getClass()](#getClass--) |  |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | Предоставляет доступ к заполнению и форматированию линий этой точки данных. |
| [getIndex()](#getIndex--) | Индекс точки данных, к которой этот объект применяет форматирование. |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [getMarker()](#getMarker--) |  |
| [hashCode()](#hashCode--) |  |
| [materializeSpPr()](#materializeSpPr--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


Очищает формат этой точки данных. Для свойств устанавливаются значения по умолчанию, определенные в родительском ряду.

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
### getBubble3D() {#getBubble3D--}
```
public boolean getBubble3D()
```


Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getExplosion() {#getExplosion--}
```
public int getExplosion()
```


Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным, отрицательное значение означает, что свойство не задано и не должно применяться разнесение. Применяется только к круговым диаграммам.

**Возвращает:**
инт
### getFormat() {#getFormat--}
```
public ChartFormat getFormat()
```


Предоставляет доступ к заполнению и форматированию линий этой точки данных.

**Возвращает:**
[ChartFormat](../../com.aspose.words/chartformat) - соответствующий[ChartFormat](../../com.aspose.words/chartformat) ценность.
### getIndex() {#getIndex--}
```
public int getIndex()
```


Индекс точки данных, к которой этот объект применяет форматирование.

**Возвращает:**
int - соответствующее значение int.
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

**Возвращает:**
логический
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


Указывает маркер данных. Маркер создается автоматически по запросу.

**Возвращает:**
[ChartMarker](../../com.aspose.words/chartmarker)
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### materializeSpPr() {#materializeSpPr--}
```
public void materializeSpPr()
```




### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBubble3D(boolean value) {#setBubble3D-boolean-}
```
public void setBubble3D(boolean value)
```


Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

### setExplosion(int value) {#setExplosion-int-}
```
public void setExplosion(int value)
```


Определяет величину, на которую точка данных должна быть перемещена от центра круговой диаграммы. Может быть отрицательным, отрицательное значение означает, что свойство не задано и не должно применяться разнесение. Применяется только к круговым диаграммам.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public void setInvertIfNegative(boolean value)
```


Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  |

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
