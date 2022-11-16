---
title: WarningInfoCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет типизированную коллекцию объектов.
type: docs
weight: 605
url: /ru/java/com.aspose.words/warninginfocollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback), java.lang.Итерабельный
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

 Представляет типизированную коллекцию[WarningInfo](../../com.aspose.words/warninginfo) объекты.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.

 Вы можете использовать этот объект коллекции как простейшую форму[IWarningCallback](../../com.aspose.words/iwarningcallback) реализация для сбора всех предупреждений, которые Aspose.Words генерирует во время операции загрузки или сохранения. Создайте экземпляр этого класса и назначьте его[LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions\#getWarningCallback--) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions\#setWarningCallback-com.aspose.words.IWarningCallback-) или же[DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase\#getWarningCallback--) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase\#setWarningCallback-com.aspose.words.IWarningCallback-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает элемент по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) |  Реализует[IWarningCallback](../../com.aspose.words/iwarningcallback) интерфейс. |
### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

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
public WarningInfo get(int index)
```


Получает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс элемента. |

**Возвращает:**
[WarningInfo](../../com.aspose.words/warninginfo) - Элемент по указанному индексу.
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


Получает количество элементов, содержащихся в коллекции.

**Возвращает:**
int - количество элементов, содержащихся в коллекции.
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


Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции.

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

### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public void warning(WarningInfo info)
```


 Реализует[IWarningCallback](../../com.aspose.words/iwarningcallback) интерфейс. Добавляет предупреждение в эту коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |
