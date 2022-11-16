---
title: AxisBound
second_title: Справочник по API Aspose.Words для Java
description: Представляет минимальную или максимальную границу значений оси.
type: docs
weight: 16
url: /ru/java/com.aspose.words/axisbound/
---

**Наследование:**
java.lang.Object
```
public class AxisBound
```

Представляет минимальную или максимальную границу значений оси.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.

Привязка может быть указана как числовое значение, дата-время или специальное значение "auto".

Экземпляры этого класса неизменяемы.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [AxisBound()](#AxisBound--) | Создает новый экземпляр, указывающий, что привязка оси должна автоматически определяться приложением для обработки текста. |
| [AxisBound(double value)](#AxisBound-double-) | Создает привязку оси, представленную в виде числа. |
| [AxisBound(Date datetime)](#AxisBound-java.util.Date-) | Создает привязку оси, представленную как значение даты и времени. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getClass()](#getClass--) |  |
| [getValue()](#getValue--) | Возвращает числовое значение связанной оси. |
| [getValueAsDate()](#getValueAsDate--) | Возвращает значение привязки оси, представленное в виде даты и времени. |
| [hashCode()](#hashCode--) |  |
| [isAuto()](#isAuto--) | Возвращает флаг, указывающий, что граница оси должна быть определена автоматически. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | Возвращает удобную для пользователя строку, отображающую значение этого объекта. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AxisBound() {#AxisBound--}
```
public AxisBound()
```


Создает новый экземпляр, указывающий, что привязка оси должна автоматически определяться приложением для обработки текста.

### AxisBound(double value) {#AxisBound-double-}
```
public AxisBound(double value)
```


Создает привязку оси, представленную в виде числа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |

### AxisBound(Date datetime) {#AxisBound-java.util.Date-}
```
public AxisBound(Date datetime)
```


Создает привязку оси, представленную как значение даты и времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| datetime | java.util.Date |  |

### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getValue() {#getValue--}
```
public double getValue()
```


Возвращает числовое значение связанной оси.

**Возвращает:**
double - Числовое значение привязки оси.
### getValueAsDate() {#getValueAsDate--}
```
public Date getValueAsDate()
```


Возвращает значение привязки оси, представленное в виде даты и времени.

**Возвращает:**
java.util.Date — значение связанной оси, представленное в виде даты и времени.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


Возвращает флаг, указывающий, что граница оси должна быть определена автоматически.

**Возвращает:**
boolean - флаг, указывающий, что привязка оси должна определяться автоматически.
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


Возвращает удобную для пользователя строку, отображающую значение этого объекта.

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
