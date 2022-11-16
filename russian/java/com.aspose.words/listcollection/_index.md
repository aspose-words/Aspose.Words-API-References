---
title: ListCollection
second_title: Справочник по API Aspose.Words для Java
description: Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе.
type: docs
weight: 369
url: /ru/java/com.aspose.words/listcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListCollection implements Cloneable, Iterable
```

Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе.

 Чтобы узнать больше, посетите**Working with Lists** документальная статья.

 Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Форматирование списков сохраняется в[ListCollection](../../com.aspose.words/listcollection) сбор отдельно от абзацев текста.

 Вы не создаете объекты этого класса. Всегда есть только один[ListCollection](../../com.aspose.words/listcollection) объекта для каждого документа, и он доступен через[DocumentBase.getLists()](../../com.aspose.words/documentbase\#getLists--) имущество.

 Чтобы создать новый список на основе предопределенного шаблона списка или на основе стиля списка, используйте кнопку[add(com.aspose.words.Style)](../../com.aspose.words/listcollection\#add-com.aspose.words.Style-) метод.

 Чтобы создать новый список с форматированием, идентичным существующему списку, используйте[addCopy(com.aspose.words.List)](../../com.aspose.words/listcollection\#addCopy-com.aspose.words.List-) метод.

 Чтобы сделать абзац маркированным или пронумерованным, необходимо применить форматирование списка к абзацу, назначив[List](../../com.aspose.words/list) возражать против[ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) свойство[ListFormat](../../com.aspose.words/listformat).

Чтобы удалить форматирование списка из абзаца, используйте[ListFormat.removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--) метод.

Если вы немного знакомы с WordprocessingML, то, возможно, знаете, что он определяет отдельные понятия для «списка» и «определения списка». Это точно соответствует тому, как форматирование списка хранится в документе Microsoft Word на низком уровне. Определение списка похоже на «схему», а список — на экземпляр определения списка.

Чтобы упростить модель программирования, Aspose.Words скрывает различие между списком и определением списка почти так же, как Microsoft Word скрывает это в своем пользовательском интерфейсе. Это позволяет вам больше сосредоточиться на том, как должен выглядеть ваш документ, а не на создании низкоуровневых объектов для удовлетворения требований формата файла Microsoft Word.

Невозможно удалить списки после их создания в текущей версии Aspose.Words. Это похоже на Microsoft Word, где пользователь не имеет явного контроля над определениями списков.
## Методы

| Метод | Описание |
| --- | --- |
| [add(Style listStyle)](#add-com.aspose.words.Style-) | Создает новый список, который ссылается на стиль списка, и добавляет его в коллекцию списков в документе. |
| [add(int listTemplate)](#add-int-) |  |
| [addCopy(List srcList)](#addCopy-com.aspose.words.List-) | Создает новый список, копируя указанный список и добавляя его в коллекцию списков в документе. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает список по индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество нумерованных и маркированных списков в документе. |
| [getDocument()](#getDocument--) | Получает документ владельца. |
| [getListByListId(int listId)](#getListByListId-int-) | Получает список по идентификатору списка. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Получает объект перечислителя, который будет перечислять списки в документе. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(Style listStyle) {#add-com.aspose.words.Style-}
```
public List add(Style listStyle)
```


Создает новый список, который ссылается на стиль списка, и добавляет его в коллекцию списков в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listStyle | [Style](../../com.aspose.words/style) | Стиль списка. |

**Возвращает:**
[List](../../com.aspose.words/list) - Недавно созданный список.

Вновь созданный список ссылается на стиль списка. Если вы измените свойства стиля списка, это отразится в свойствах списка. И наоборот, если вы измените свойства списка, это отразится на свойствах стиля списка.
### add(int listTemplate) {#add-int-}
```
public List add(int listTemplate)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplate | int |  |

**Возвращает:**
[List](../../com.aspose.words/list)
### addCopy(List srcList) {#addCopy-com.aspose.words.List-}
```
public List addCopy(List srcList)
```


Создает новый список, копируя указанный список и добавляя его в коллекцию списков в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcList | [List](../../com.aspose.words/list) | Список источников для копирования. |

**Возвращает:**
[List](../../com.aspose.words/list) - Недавно созданный список.

Список источников может быть из любого документа. Если исходный список принадлежит другому документу, копия списка создается и добавляется в текущий документ.

Если исходный список является ссылкой или определением стиля списка, вновь созданный список не связан с исходным стилем списка.
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
public List get(int index)
```


Получает список по индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

**Возвращает:**
[List](../../com.aspose.words/list) - Список по индексу.
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


Получает количество нумерованных и маркированных списков в документе.

**Возвращает:**
int — количество нумерованных и маркированных списков в документе.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ владельца.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ собственника.
### getListByListId(int listId) {#getListByListId-int-}
```
public List getListByListId(int listId)
```


Получает список по идентификатору списка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| listId | int | Идентификатор списка. |

**Возвращает:**
[List](../../com.aspose.words/list) - Возвращает объект списка. Возвращает null, если список с указанным идентификатором не найден.

 Обычно вам не нужно использовать этот метод. В большинстве случаев вы применяете форматирование списка к абзацам, просто устанавливая[ListFormat.getList()](../../com.aspose.words/listformat\#getList--) / [ListFormat.setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) собственность[ListFormat](../../com.aspose.words/listformat) объект.
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


Получает объект перечислителя, который будет перечислять списки в документе.

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
