---
title: NodeList
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор узлов, соответствующих запросу XPath, выполненному с использованием метода.
type: docs
weight: 406
url: /ru/java/com.aspose.words/nodelist/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class NodeList implements Iterable
```

 Представляет набор узлов, соответствующих запросу XPath, выполненному с использованием[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) метод.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

**NodeList** возвращается[CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) и содержит набор узлов, соответствующих запросу XPath.

**NodeList** поддерживает индексированный доступ и итерацию.

 лечить**NodeList** коллекция как коллекция "моментальных снимков".**NodeList** запускается как «живая» коллекция, поскольку узлы фактически не извлекаются при выполнении запроса XPath. Узлы извлекаются только при доступе, и в это время узел и все предшествующие ему узлы кэшируются, образуя коллекцию «моментальных снимков».
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Извлекает узел по заданному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество узлов в списке. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Обеспечивает простую итерацию в стиле foreach по набору узлов. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toArray()](#toArray--) | Копирует все узлы из коллекции в новый массив узлов. |
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
### get(int index) {#get-int-}
```
public Node get(int index)
```


Извлекает узел по заданному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в списке узлов. |

**Возвращает:**
[Node](../../com.aspose.words/node) - соответствующий[Node](../../com.aspose.words/node) ценность.
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


Получает количество узлов в списке.

**Возвращает:**
int - количество узлов в списке.
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


Обеспечивает простую итерацию в стиле foreach по набору узлов.

**Возвращает:**
java.util.Iterator — итератор.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toArray() {#toArray--}
```
public Node[] toArray()
```


Копирует все узлы из коллекции в новый массив узлов.

Вы не должны добавлять/удалять узлы при переборе коллекции узлов, потому что это делает итератор недействительным и требует обновления для живых коллекций.

Чтобы иметь возможность добавлять/удалять узлы во время итерации, используйте этот метод для копирования узлов в массив фиксированного размера, а затем выполните итерацию по массиву.

**Возвращает:**
com.aspose.words.Node[] - Массив узлов.
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
