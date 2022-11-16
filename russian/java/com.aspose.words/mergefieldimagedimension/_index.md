---
title: MergeFieldImageDimension
second_title: Справочник по API Aspose.Words для Java
description: Представляет размер изображения, т.е.
type: docs
weight: 394
url: /ru/java/com.aspose.words/mergefieldimagedimension/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class MergeFieldImageDimension implements Cloneable
```

Представляет размер изображения (т. е. ширину или высоту), используемый в процессе слияния.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

 Чтобы указать, что изображение должно быть вставлено с исходным размером во время слияния, вы должны присвоить отрицательное значение параметру[getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) имущество.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [MergeFieldImageDimension(double value)](#MergeFieldImageDimension-double-) | Создает экземпляр размера изображения с заданным значением в пунктах. |
| [MergeFieldImageDimension(double value, int unit)](#MergeFieldImageDimension-double-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getUnit()](#getUnit--) | Единица. |
| [getValue()](#getValue--) | Значение. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setUnit(int value)](#setUnit-int-) | Единица. |
| [setValue(double value)](#setValue-double-) | Значение. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### MergeFieldImageDimension(double value) {#MergeFieldImageDimension-double-}
```
public MergeFieldImageDimension(double value)
```


Создает экземпляр размера изображения с заданным значением в пунктах. Вы должны использовать отрицательное значение, чтобы указать, что исходное значение соответствующего размера изображения должно быть применено.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Значение. |

### MergeFieldImageDimension(double value, int unit) {#MergeFieldImageDimension-double-int-}
```
public MergeFieldImageDimension(double value, int unit)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double |  |
| unit | int |  |

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
### getUnit() {#getUnit--}
```
public int getUnit()
```


Единица.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit) константы.
### getValue() {#getValue--}
```
public double getValue()
```


Значение. Вы должны использовать отрицательное значение, чтобы указать, что исходное значение соответствующего размера изображения должно быть применено.

**Возвращает:**
double - соответствующее двойное значение.
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




### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


Единица.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit) константы. |

### setValue(double value) {#setValue-double-}
```
public void setValue(double value)
```


Значение. Вы должны использовать отрицательное значение, чтобы указать, что исходное значение соответствующего размера изображения должно быть применено.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

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
