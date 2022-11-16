---
title: TextColumn
second_title: Справочник по API Aspose.Words для Java
description: Представляет один текстовый столбец.
type: docs
weight: 561
url: /ru/java/com.aspose.words/textcolumn/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

 Представляет один текстовый столбец.**TextColumn** является членом[TextColumnCollection](../../com.aspose.words/textcolumncollection) коллекция.**TextColumns** коллекция включает в себя все столбцы в разделе документа.

 Чтобы узнать больше, посетите**Working with Sections** документальная статья.

**TextColumn** объекты используются только для указания столбцов с пользовательской шириной и интервалом. Если вы хотите, чтобы столбцы в документе были одинаковой ширины, установите TextColumns.[TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) к**true**.

 Когда новый**TextColumn** создается, его ширина и интервал равны нулю.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getSpaceAfter()](#getSpaceAfter--) | Получает расстояние между этим столбцом и следующим столбцом в пунктах. |
| [getWidth()](#getWidth--) | Получает ширину текстового столбца в пунктах. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setSpaceAfter(double value)](#setSpaceAfter-double-) | Устанавливает расстояние между этим столбцом и следующим столбцом в пунктах. |
| [setWidth(double value)](#setWidth-double-) | Устанавливает ширину текстового столбца в пунктах. |
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
### getSpaceAfter() {#getSpaceAfter--}
```
public double getSpaceAfter()
```


Получает расстояние между этим столбцом и следующим столбцом в пунктах. Не требуется для последнего столбца.

**Возвращает:**
double - Пространство между этим столбцом и следующим столбцом в пунктах.
### getWidth() {#getWidth--}
```
public double getWidth()
```


Получает ширину текстового столбца в пунктах.

**Возвращает:**
double - Ширина текстового столбца в пунктах.
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




### setSpaceAfter(double value) {#setSpaceAfter-double-}
```
public void setSpaceAfter(double value)
```


Устанавливает расстояние между этим столбцом и следующим столбцом в пунктах. Не требуется для последнего столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Пространство между этим столбцом и следующим столбцом в пунктах. |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Устанавливает ширину текстового столбца в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Ширина текстового столбца в пунктах. |

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
