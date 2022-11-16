---
title: ChartSeries
second_title: Справочник по API Aspose.Words для Java
description: Представляет свойства ряда диаграммы.
type: docs
weight: 68
url: /ru/java/com.aspose.words/chartseries/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

Представляет свойства ряда диаграммы.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [getClass()](#getClass--) |  |
| [getDataLabels()](#getDataLabels--) | Указывает параметры меток данных для всего ряда. |
| [getDataPoints()](#getDataPoints--) | Возвращает коллекцию объектов форматирования для всех точек данных в этой серии. |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | Предоставляет доступ к заливке и форматированию строк серии. |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [getLegendEntry()](#getLegendEntry--) | Получает легенду для этой серии диаграмм. |
| [getMarker()](#getMarker--) |  |
| [getName()](#getName--) | Получает имя серии, если имя не указано явно, оно генерируется с использованием индекса. |
| [getSmooth()](#getSmooth--) | Позволяет указать, следует ли сглаживать линию, соединяющую точки на графике, с помощью сплайнов Катмулла-Рома. |
| [hasDataLabels()](#hasDataLabels--) | Получает флаг, указывающий, отображаются ли метки данных для ряда. |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean-) | Устанавливает флаг, указывающий, отображаются ли метки данных для ряда. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [setName(String value)](#setName-java.lang.String-) | Задает имя серии, если имя не задано явно, оно генерируется с использованием индекса. |
| [setSmooth(boolean value)](#setSmooth-boolean-) | Позволяет указать, следует ли сглаживать линию, соединяющую точки на графике, с помощью сплайнов Катмулла-Рома. |
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
### getDataLabels() {#getDataLabels--}
```
public ChartDataLabelCollection getDataLabels()
```


Указывает параметры меток данных для всего ряда.

**Возвращает:**
[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) - соответствующий[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) ценность.
### getDataPoints() {#getDataPoints--}
```
public ChartDataPointCollection getDataPoints()
```


Возвращает коллекцию объектов форматирования для всех точек данных в этой серии.

**Возвращает:**
[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) - Коллекция объектов форматирования для всех точек данных в этой серии.
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


Предоставляет доступ к заливке и форматированию строк серии.

**Возвращает:**
[ChartFormat](../../com.aspose.words/chartformat) - соответствующий[ChartFormat](../../com.aspose.words/chartformat) ценность.
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное.

**Возвращает:**
логический
### getLegendEntry() {#getLegendEntry--}
```
public ChartLegendEntry getLegendEntry()
```


Получает легенду для этой серии диаграмм.

**Возвращает:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry) - Запись легенды для этой серии диаграмм.
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


Указывает маркер данных. Маркер создается автоматически по запросу.

**Возвращает:**
[ChartMarker](../../com.aspose.words/chartmarker)
### getName() {#getName--}
```
public String getName()
```


Получает имя серии, если имя не указано явно, оно генерируется с использованием индекса. По умолчанию возвращает серию плюс один основанный индекс.

**Возвращает:**
java.lang.String — Имя серии, если имя не задано явно, оно генерируется с использованием индекса.
### getSmooth() {#getSmooth--}
```
public boolean getSmooth()
```


Позволяет указать, следует ли сглаживать линию, соединяющую точки на графике, с помощью сплайнов Катмулла-Рома.

**Возвращает:**
boolean - соответствующее логическое значение.
### hasDataLabels() {#hasDataLabels--}
```
public boolean hasDataLabels()
```


Получает флаг, указывающий, отображаются ли метки данных для ряда.

**Возвращает:**
boolean — Флаг, указывающий, отображаются ли метки данных для ряда.
### hasDataLabels(boolean value) {#hasDataLabels-boolean-}
```
public void hasDataLabels(boolean value)
```


Устанавливает флаг, указывающий, отображаются ли метки данных для ряда.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, отображаются ли метки данных для ряда. |

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

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Задает имя серии, если имя не задано явно, оно генерируется с использованием индекса. По умолчанию возвращает серию плюс один основанный индекс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название серии, если имя не задано явно, генерируется с использованием index. |

### setSmooth(boolean value) {#setSmooth-boolean-}
```
public void setSmooth(boolean value)
```


Позволяет указать, следует ли сглаживать линию, соединяющую точки на графике, с помощью сплайнов Катмулла-Рома.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
