---
title: CustomXmlSchemaCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция строк, представляющих схемы XML, связанные с настраиваемой частью XML.
type: docs
weight: 108
url: /ru/java/com.aspose.words/customxmlschemacollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class CustomXmlSchemaCollection implements Iterable
```

Коллекция строк, представляющих схемы XML, связанные с настраиваемой частью XML.

 Чтобы узнать больше, посетите**Structured Document Tags or Content Control** документальная статья.

 Вы не создаете экземпляры этого класса. Вы получаете доступ к набору XML-схем пользовательской XML-части через[CustomXmlPart.getSchemas()](../../com.aspose.words/customxmlpart\#getSchemas--) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [add(String value)](#add-java.lang.String-) | Добавляет элемент в коллекцию. |
| [clear()](#clear--) | Удаляет все элементы из коллекции. |
| [deepClone()](#deepClone--) | Делает глубокий клон этого объекта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Получает элемент по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Получает количество элементов, содержащихся в коллекции. |
| [hashCode()](#hashCode--) |  |
| [indexOf(String value)](#indexOf-java.lang.String-) | Возвращает отсчитываемый от нуля индекс указанного значения в коллекции. |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет указанное значение из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет значение по указанному индексу. |
| [set(int index, String value)](#set-int-java.lang.String-) | Устанавливает элемент по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String value) {#add-java.lang.String-}
```
public void add(String value)
```


Добавляет элемент в коллекцию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Элемент для добавления. |

### clear() {#clear--}
```
public void clear()
```


Удаляет все элементы из коллекции.

### deepClone() {#deepClone--}
```
public CustomXmlSchemaCollection deepClone()
```


Делает глубокий клон этого объекта.

**Возвращает:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection)
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
public String get(int index)
```


Получает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |

**Возвращает:**
java.lang.String — элемент по указанному индексу.
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
### indexOf(String value) {#indexOf-java.lang.String-}
```
public int indexOf(String value)
```


Возвращает отсчитываемый от нуля индекс указанного значения в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Значение с учетом регистра для поиска. |

**Возвращает:**
int - индекс, основанный на нуле. Отрицательное значение, если не найдено.
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




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Удаляет указанное значение из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Удаляемое значение с учетом регистра. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет значение по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### set(int index, String value) {#set-int-java.lang.String-}
```
public void set(int index, String value)
```


Устанавливает элемент по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |
| value | java.lang.String | Элемент по указанному индексу. |

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
