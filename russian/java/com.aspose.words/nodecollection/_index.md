---
title: NodeCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор узлов определенного типа.
type: docs
weight: 404
url: /ru/java/com.aspose.words/nodecollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class NodeCollection implements Iterable
```

Представляет набор узлов определенного типа.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

**NodeCollection**не владеет узлами, которые он содержит, скорее, это просто выбор узлов указанного типа, но узлы хранятся в дереве под соответствующими родительскими узлами.

**NodeCollection** поддерживает индексированный доступ, итерацию и предоставляет методы добавления и удаления.

**NodeCollection** коллекция является «живой», т. е. изменения дочерних объектов узла, из которого она была создана, немедленно отражаются в узлах, возвращаемых**NodeCollection** свойства и методы.

**NodeCollection** возвращается**M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** а также служит базовым классом для наборов типизированных узлов, таких как[SectionCollection](../../com.aspose.words/sectioncollection), [ParagraphCollection](../../com.aspose.words/paragraphcollection) и т.п.

**NodeCollection** может быть «плоским» и содержать только непосредственных дочерних элементов узла, из которого он был создан, или он может быть «глубоким» и содержать всех дочерних элементов.
## Методы

| Метод | Описание |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node-) | Добавляет узел в конец коллекции. |
| [clear()](#clear--) | Удаляет все узлы из этой коллекции и из документа. |
| [contains(Node node)](#contains-com.aspose.words.Node-) | Определяет, находится ли узел в коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Извлекает узел по заданному индексу. |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Получает количество узлов в коллекции. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node-) | Возвращает отсчитываемый от нуля индекс указанного узла. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node-) | Вставляет узел в коллекцию по указанному индексу. |
| [iterator()](#iterator--) | Обеспечивает простую итерацию в стиле foreach по набору узлов. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Node node)](#remove-com.aspose.words.Node-) | Удаляет узел из коллекции и из документа. |
| [removeAt(int index)](#removeAt-int-) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [toArray()](#toArray--) | Копирует все узлы из коллекции в новый массив узлов. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(Node node) {#add-com.aspose.words.Node-}
```
public void add(Node node)
```


Добавляет узел в конец коллекции.

Узел вставляется как дочерний в объект узла, из которого была создана коллекция.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | Узел, который нужно добавить в конец коллекции. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все узлы из этой коллекции и из документа.

### contains(Node node) {#contains-com.aspose.words.Node-}
```
public boolean contains(Node node)
```


Определяет, находится ли узел в коллекции.

Этот метод выполняет линейный поиск; следовательно, среднее время выполнения пропорционально Count.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | Узел, который необходимо найти. |

**Возвращает:**
boolean - Истинно, если элемент найден в коллекции; в противном случае ложно.
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

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции узлов.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

 Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.|

**Возвращает:**
[Node](../../com.aspose.words/node) - соответствующий[Node](../../com.aspose.words/node) ценность.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество узлов в коллекции.

**Возвращает:**
int — количество узлов в коллекции.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Возвращает:**
[Node](../../com.aspose.words/node)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### indexOf(Node node) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node node)
```


Возвращает отсчитываемый от нуля индекс указанного узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | Узел, который необходимо найти. |

**Возвращает:**
int — Отсчитываемый от нуля индекс узла в коллекции, если он найден; иначе -1.

Этот метод выполняет линейный поиск; следовательно, среднее время выполнения пропорционально Count.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node-}
```
public void insert(int index, Node node)
```


Вставляет узел в коллекцию по указанному индексу.

Узел вставляется как дочерний в объект узла, из которого была создана коллекция.

Если индекс равен или больше Count, узел добавляется в конец коллекции.

Если индекс отрицательный и его абсолютное значение больше, чем Count, узел добавляется в конец коллекции.

Если новый дочерний элемент уже находится в дереве, он сначала удаляется.

 Если вставляемый узел был создан из другого документа, следует использовать**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** чтобы импортировать узел в текущий документ. Затем импортированный узел можно вставить в текущий документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс узла. Отрицательные индексы разрешены и указывают на доступ из конца списка. Например, -1 означает последний узел, -2 означает предпоследний и так далее. |
| node | [Node](../../com.aspose.words/node) | Узел для вставки. |

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




### remove(Node node) {#remove-com.aspose.words.Node-}
```
public void remove(Node node)
```


Удаляет узел из коллекции и из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | Узел для удаления. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет узел с указанным индексом из коллекции и из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс узла. Отрицательные индексы разрешены и указывают на доступ из конца списка. Например, -1 означает последний узел, -2 означает предпоследний и так далее. |

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
