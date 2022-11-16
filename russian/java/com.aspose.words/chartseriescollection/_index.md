---
title: ChartSeriesCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию файла .
type: docs
weight: 69
url: /ru/java/com.aspose.words/chartseriescollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class ChartSeriesCollection implements Iterable
```

 Представляет собой коллекцию[ChartSeries](../../com.aspose.words/chartseries).

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double---) | Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double---) | Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double---) | Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double---) | Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. |
| [clear()](#clear--) |  Удаляет все[ChartSeries](../../com.aspose.words/chartseries) из этой коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Возвращает[ChartSeries](../../com.aspose.words/chartseries) по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  Возвращает количество[ChartSeries](../../com.aspose.words/chartseries) в этой коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) |  Удаляет[ChartSeries](../../com.aspose.words/chartseries) по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues)
```


Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. Используйте этот метод для добавления рядов к любому типу точечных диаграмм.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |

**Возвращает:**
[ChartSeries](../../com.aspose.words/chartseries) - Недавно добавленный[ChartSeries](../../com.aspose.words/chartseries) объект.
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```


Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. Используйте этот метод для добавления рядов в пузырьковые диаграммы любого типа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |
| bubbleSizes | double[] |  |

**Возвращает:**
[ChartSeries](../../com.aspose.words/chartseries) - Недавно добавленный[ChartSeries](../../com.aspose.words/chartseries) объект.
### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double---}
```
public ChartSeries add(String seriesName, String[] categories, double[] values)
```


Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. Используйте этот метод, чтобы добавить ряды к любому типу линейчатых, столбчатых, линейных и поверхностных диаграмм.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | java.lang.String[] |  |
| values | double[] |  |

**Возвращает:**
[ChartSeries](../../com.aspose.words/chartseries) - Недавно добавленный[ChartSeries](../../com.aspose.words/chartseries) объект.
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double---}
```
public ChartSeries add(String seriesName, Date[] dates, double[] values)
```


Добавляет новые[ChartSeries](../../com.aspose.words/chartseries) к этой коллекции. Используйте этот метод, чтобы добавить ряды к любому типу площадных, радарных и фондовых диаграмм.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| dates | java.util.Date[] |  |
| values | double[] |  |

**Возвращает:**
[ChartSeries](../../com.aspose.words/chartseries)
### clear() {#clear--}
```
public void clear()
```


 Удаляет все[ChartSeries](../../com.aspose.words/chartseries) из этой коллекции.

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
### get(int index) {#get-int-}
```
public ChartSeries get(int index)
```


 Возвращает[ChartSeries](../../com.aspose.words/chartseries) по указанному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[ChartSeries](../../com.aspose.words/chartseries) - А[ChartSeries](../../com.aspose.words/chartseries) по указанному индексу.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCount() {#getCount--}
```
public int getCount()
```


 Возвращает количество[ChartSeries](../../com.aspose.words/chartseries) в этой коллекции.

**Возвращает:**
 int - количество[ChartSeries](../../com.aspose.words/chartseries) в этой коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Возвращает:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


 Удаляет[ChartSeries](../../com.aspose.words/chartseries) по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс удаляемой серии ChartSeries. |

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
