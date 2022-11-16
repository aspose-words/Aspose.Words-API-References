---
title: TabStopCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих настраиваемые вкладки для абзаца или стиля.
type: docs
weight: 547
url: /ru/java/com.aspose.words/tabstopcollection/
---

**Наследование:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class TabStopCollection extends InternableComplexAttr implements Cloneable
```

 Коллекция[TabStop](../../com.aspose.words/tabstop) объекты, представляющие настраиваемые вкладки для абзаца или стиля.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

В документах Microsoft Word позицию табуляции можно определить в свойствах стиля абзаца или непосредственно в свойствах абзаца. Стиль может быть основан на другом стиле. Таким образом, полный набор позиций табуляции для данного объекта представляет собой комбинацию позиций табуляции, определенных непосредственно для этого объекта, и позиций табуляции, унаследованных от родительских стилей.

 В Aspose.Words при получении**TabStops**коллекция для абзаца или стиля, она содержит только настраиваемые позиции табуляции, определенные непосредственно для этого абзаца или стиля. Коллекция не включает позиции табуляции, определенные в родительских стилях или позиции табуляции по умолчанию.
## Методы

| Метод | Описание |
| --- | --- |
| [add(TabStop tabStop)](#add-com.aspose.words.TabStop-) | Добавляет или заменяет позицию табуляции в коллекции. |
| [add(double position, int alignment, int leader)](#add-double-int-int-) |  |
| [after(double position)](#after-double-) | Получает первую позицию табуляции справа от указанной позиции. |
| [before(double position)](#before-double-) | Получает первую позицию табуляции слева от указанной позиции. |
| [clear()](#clear--) | Удаляет все позиции табуляции. |
| [equals(TabStopCollection rhs)](#equals-com.aspose.words.TabStopCollection-) | Определяет, равна ли заданная коллекция TabStopCollection по значению текущей коллекции TabStopCollection. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get(double position)](#get-double-) | Получает позицию табуляции в указанной позиции. |
| [get(int index)](#get-int-) | Извлекает позицию табуляции из коллекции. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество позиций табуляции в коллекции. |
| [getIndexByPosition(double position)](#getIndexByPosition-double-) | Получает индекс позиции табуляции с указанной позицией в пунктах. |
| [getPositionByIndex(int index)](#getPositionByIndex-int-) | Получает позицию (в пунктах) позиции табуляции по указанному индексу. |
| [hashCode()](#hashCode--) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeByIndex(int index)](#removeByIndex-int-) | Удаляет позицию табуляции по указанному индексу из коллекции. |
| [removeByPosition(double position)](#removeByPosition-double-) | Удаляет позицию табуляции в указанной позиции из коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(TabStop tabStop) {#add-com.aspose.words.TabStop-}
```
public void add(TabStop tabStop)
```


Добавляет или заменяет позицию табуляции в коллекции.

Если табуляция уже существует в указанной позиции, она заменяется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tabStop | [TabStop](../../com.aspose.words/tabstop) | Объект табуляции для добавления. |

### add(double position, int alignment, int leader) {#add-double-int-int-}
```
public void add(double position, int alignment, int leader)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### after(double position) {#after-double-}
```
public TabStop after(double position)
```


Получает первую позицию табуляции справа от указанной позиции.

 Пропускает позиции табуляции с помощью**Alignment** установите TabAlignment.Bar .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double | Контрольная позиция (в пунктах). |

**Возвращает:**
[TabStop](../../com.aspose.words/tabstop) - Объект табуляции или ноль, если подходящая табуляция не найдена.
### before(double position) {#before-double-}
```
public TabStop before(double position)
```


Получает первую позицию табуляции слева от указанной позиции.

 Пропускает позиции табуляции с помощью**Alignment** установите TabAlignment.Bar .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double | Контрольная позиция (в пунктах). |

**Возвращает:**
[TabStop](../../com.aspose.words/tabstop) - Объект табуляции или ноль, если подходящая табуляция не найдена.
### clear() {#clear--}
```
public void clear()
```


Удаляет все позиции табуляции.

### equals(TabStopCollection rhs) {#equals-com.aspose.words.TabStopCollection-}
```
public boolean equals(TabStopCollection rhs)
```


Определяет, равна ли заданная коллекция TabStopCollection по значению текущей коллекции TabStopCollection.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rhs | [TabStopCollection](../../com.aspose.words/tabstopcollection) |  |

**Возвращает:**
логический
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
### get(double position) {#get-double-}
```
public TabStop get(double position)
```


Получает позицию табуляции в указанной позиции. Возвращает null, если в указанной позиции не найдена табуляция.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double | Положение (в пунктах) табуляции. |

**Возвращает:**
[TabStop](../../com.aspose.words/tabstop) - Табуляция в указанной позиции.
### get(int index) {#get-int-}
```
public TabStop get(int index)
```


Извлекает позицию табуляции из коллекции. Получает позицию табуляции по заданному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Указатель в коллекции позиций табуляции. |

**Возвращает:**
[TabStop](../../com.aspose.words/tabstop) - соответствующий[TabStop](../../com.aspose.words/tabstop) ценность.
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


Получает количество позиций табуляции в коллекции.

**Возвращает:**
int — количество позиций табуляции в коллекции.
### getIndexByPosition(double position) {#getIndexByPosition-double-}
```
public int getIndexByPosition(double position)
```


Получает индекс позиции табуляции с указанной позицией в пунктах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double |  |

**Возвращает:**
инт
### getPositionByIndex(int index) {#getPositionByIndex-int-}
```
public double getPositionByIndex(int index)
```


Получает позицию (в пунктах) позиции табуляции по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Указатель в коллекции позиций табуляции. |

**Возвращает:**
double - Позиция табуляции.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
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




### removeByIndex(int index) {#removeByIndex-int-}
```
public void removeByIndex(int index)
```


Удаляет позицию табуляции по указанному индексу из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Указатель в коллекции позиций табуляции. |

### removeByPosition(double position) {#removeByPosition-double-}
```
public void removeByPosition(double position)
```


Удаляет позицию табуляции в указанной позиции из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| position | double | Позиция (в пунктах) позиции табуляции, которую нужно удалить. |

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
