---
title: CustomXmlPartCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет коллекцию пользовательских XML-частей.
type: docs
weight: 105
url: /ru/java/com.aspose.words/customxmlpartcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class CustomXmlPartCollection implements Iterable
```

 Представляет коллекцию пользовательских XML-частей. Элементы[CustomXmlPart](../../com.aspose.words/customxmlpart) объекты.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

Обычно вам не нужно создавать экземпляры этого класса. Вы можете получить доступ к пользовательским XML-данным, хранящимся в документе, через[Document.getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [add(CustomXmlPart part)](#add-com.aspose.words.CustomXmlPart-) | Добавляет элемент в коллекцию. |
| [add(String id, String xml)](#add-java.lang.String-java.lang.String-) | Создает новую часть XML с указанным XML и добавляет ее в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [deepClone()](#deepClone--) | Создает глубокую копию этой коллекции и ее элементов. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает элемент по указанному индексу. |
| [getById(String id)](#getById-java.lang.String-) | Находит и возвращает пользовательскую часть XML по ее идентификатору. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | Удаляет элемент по указанному индексу. |
| [set(int index, CustomXmlPart value)](#set-int-com.aspose.words.CustomXmlPart-) | Устанавливает элемент по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(CustomXmlPart part) {#add-com.aspose.words.CustomXmlPart-}
```
public void add(CustomXmlPart part)
```


Добавляет элемент в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| part | [CustomXmlPart](../../com.aspose.words/customxmlpart) | Настраиваемая часть XML для добавления. |

### add(String id, String xml) {#add-java.lang.String-java.lang.String-}
```
public CustomXmlPart add(String id, String xml)
```


Создает новую часть XML с указанным XML и добавляет ее в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | java.lang.String | Идентификатор новой пользовательской части XML. |
| xml | java.lang.String | XML-данные детали. |

**Возвращает:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Создана пользовательская часть XML.
### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### deepClone() {#deepClone--}
```
public CustomXmlPartCollection deepClone()
```


Создает глубокую копию этой коллекции и ее элементов.

**Возвращает:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection)
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
public CustomXmlPart get(int index)
```


Получает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс элемента. |

**Возвращает:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Элемент по указанному индексу.
### getById(String id) {#getById-java.lang.String-}
```
public CustomXmlPart getById(String id)
```


Находит и возвращает пользовательскую часть XML по ее идентификатору.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| id | java.lang.String | Строка с учетом регистра, идентифицирующая пользовательскую часть XML. |

**Возвращает:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - Возвращает значение null, если пользовательская часть XML с указанным идентификатором не найдена.
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




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### set(int index, CustomXmlPart value) {#set-int-com.aspose.words.CustomXmlPart-}
```
public void set(int index, CustomXmlPart value)
```


Устанавливает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс элемента. |
| value | [CustomXmlPart](../../com.aspose.words/customxmlpart) | Элемент по указанному индексу. |

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
