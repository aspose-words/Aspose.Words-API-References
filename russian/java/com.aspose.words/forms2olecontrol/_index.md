---
title: Forms2OleControl
second_title: Справочник по API Aspose.Words для Java
description: Представляет элемент управления OLE Microsoft Forms 2.0.
type: docs
weight: 298
url: /ru/java/com.aspose.words/forms2olecontrol/
---

**Наследование:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol)
```
public abstract class Forms2OleControl extends OleControl
```

Представляет элемент управления OLE Microsoft Forms 2.0.

 Чтобы узнать больше, посетите**Working with Ole Objects** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [Forms2OleControl()](#Forms2OleControl--) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCaption()](#getCaption--) | Получает свойство Caption элемента управления. |
| [getChildNodes()](#getChildNodes--) | Получает коллекцию непосредственных дочерних элементов управления. |
| [getClass()](#getClass--) |  |
| [getEnabled()](#getEnabled--) | Возвращает true, если элемент управления находится во включенном состоянии. |
| [getName()](#getName--) | Получает имя элемента управления ActiveX. |
| [getType()](#getType--) | Получает тип элемента управления Forms 2.0. |
| [getValue()](#getValue--) | Получает базовое свойство Value, которое часто представляет состояние элемента управления. |
| [hashCode()](#hashCode--) |  |
| [isForms2OleControl()](#isForms2OleControl--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Forms2OleControl() {#Forms2OleControl--}
```
public Forms2OleControl()
```


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
### getCaption() {#getCaption--}
```
public String getCaption()
```


Получает свойство Caption элемента управления. Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — свойство заголовка элемента управления.
### getChildNodes() {#getChildNodes--}
```
public Forms2OleControlCollection getChildNodes()
```


 Получает коллекцию непосредственных дочерних элементов управления. Возвращает**null** если этот контроль не может иметь детей.

**Возвращает:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection) - Коллекция непосредственных дочерних элементов управления.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


Возвращает true, если элемент управления находится во включенном состоянии.

**Возвращает:**
boolean — Истинно, если элемент управления находится во включенном состоянии.
### getName() {#getName--}
```
public String getName()
```


Получает имя элемента управления ActiveX.

**Возвращает:**
java.lang.String — имя элемента управления ActiveX.
### getType() {#getType--}
```
public int getType()
```


Получает тип элемента управления Forms 2.0.

**Возвращает:**
 int - Тип элемента управления Forms 2.0. Возвращаемое значение является одним из[Forms2OleControlType](../../com.aspose.words/forms2olecontroltype) константы.
### getValue() {#getValue--}
```
public String getValue()
```


Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченная опция имеет значение «1», а неотмеченная — «0». Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — свойство базового значения, которое часто представляет состояние элемента управления.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isForms2OleControl() {#isForms2OleControl--}
```
public boolean isForms2OleControl()
```


 Возвращает true, если элемент управления[Forms2OleControl](../../com.aspose.words/forms2olecontrol).

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
