---
title: TabStop
second_title: Справочник по API Aspose.Words для Java
description: Представляет одну настраиваемую позицию табуляции.
type: docs
weight: 546
url: /ru/java/com.aspose.words/tabstop/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

 Представляет одну настраиваемую позицию табуляции.**TabStop** объект является членом[TabStopCollection](../../com.aspose.words/tabstopcollection) коллекция.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

 Обычно табуляция определяет позицию, в которой существует табуляция. Но поскольку позиции табуляции могут быть унаследованы от родительских стилей, может потребоваться, чтобы дочерний объект явно определял отсутствие позиции табуляции в заданной позиции. Чтобы очистить унаследованную позицию табуляции в заданной позиции, создайте**TabStop** объект и набор[getAlignment()](../../com.aspose.words/tabstop\#getAlignment--) / [setAlignment(int)](../../com.aspose.words/tabstop\#setAlignment-int-) в TabAlignment.Clear .

 Для получения дополнительной информации см.[TabStopCollection](../../com.aspose.words/tabstopcollection).
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [TabStop(double position)](#TabStop-double-) | Инициализирует новый экземпляр этого класса. |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop-) | Сравнивается с указанным TabStop. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlignment()](#getAlignment--) | Получает выравнивание текста на этой позиции табуляции. |
| [getClass()](#getClass--) |  |
| [getLeader()](#getLeader--) | Получает тип линии выноски, отображаемой под символом табуляции. |
| [getPosition()](#getPosition--) | Получает позицию табуляции в пунктах. |
| [hashCode()](#hashCode--) |  |
| [isClear()](#isClear--) | Возвращает true, если эта позиция табуляции очищает все существующие позиции табуляции в этой позиции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlignment(int value)](#setAlignment-int-) | Устанавливает выравнивание текста на этой позиции табуляции. |
| [setLeader(int value)](#setLeader-int-) | Задает тип линии выноски, отображаемой под символом табуляции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### TabStop(double position) {#TabStop-double-}
```
public TabStop(double position)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int-}
```
public TabStop(double position, int alignment, int leader)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop-}
```
public boolean equals(TabStop rhs)
```


Сравнивается с указанным TabStop.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop) |  |

**Возвращает:**
логический
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
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Получает выравнивание текста на этой позиции табуляции.

**Возвращает:**
int — выравнивание текста на этой позиции табуляции. Возвращаемое значение является одним из[TabAlignment](../../com.aspose.words/tabalignment) константы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getLeader() {#getLeader--}
```
public int getLeader()
```


Получает тип линии выноски, отображаемой под символом табуляции.

**Возвращает:**
 int — тип линии выноски, отображаемой под символом табуляции. Возвращаемое значение является одним из[TabLeader](../../com.aspose.words/tableader) константы.
### getPosition() {#getPosition--}
```
public double getPosition()
```


Получает позицию табуляции в пунктах.

**Возвращает:**
double - Положение табулятора в пунктах.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isClear() {#isClear--}
```
public boolean isClear()
```


Возвращает true, если эта позиция табуляции очищает все существующие позиции табуляции в этой позиции.

**Возвращает:**
boolean — Истинно, если эта табуляция очищает все существующие позиции табуляции в этой позиции.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Устанавливает выравнивание текста на этой позиции табуляции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Выравнивание текста на этой позиции табуляции. Значение должно быть одним из[TabAlignment](../../com.aspose.words/tabalignment) константы. |

### setLeader(int value) {#setLeader-int-}
```
public void setLeader(int value)
```


Задает тип линии выноски, отображаемой под символом табуляции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип линии выноски, отображаемой под символом табуляции. Значение должно быть одним из[TabLeader](../../com.aspose.words/tableader) константы. |

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
