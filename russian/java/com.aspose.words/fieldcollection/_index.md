---
title: FieldCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов, представляющих поля в указанном диапазоне.
type: docs
weight: 169
url: /ru/java/com.aspose.words/fieldcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class FieldCollection implements Iterable
```

 Коллекция[Field](../../com.aspose.words/field) объекты, представляющие поля в указанном диапазоне.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Экземпляр этой коллекции перебирает поля, которые начинают попадать в указанный диапазон.

[FieldCollection](../../com.aspose.words/fieldcollection) коллекция не владеет содержащимися в ней полями, а представляет собой просто набор полей.

[FieldCollection](../../com.aspose.words/fieldcollection) коллекция является «живой», т. е. изменения дочерних объектов узла, из которого она была создана, немедленно отражаются в полях, возвращаемых[FieldCollection](../../com.aspose.words/fieldcollection) свойства и методы.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все поля этой коллекции из документа и из самой этой коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает поле по указанному индексу. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество полей в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(Field field)](#remove-com.aspose.words.Field-) | Удаляет указанное поле из этой коллекции и из документа. |
| [removeAt(int index)](#removeAt-int-) | Удаляет поле с указанным индексом из этой коллекции и из документа. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


Удаляет все поля этой коллекции из документа и из самой этой коллекции.

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
public Field get(int index)
```


Возвращает поле по указанному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[Field](../../com.aspose.words/field) - Поле по указанному индексу.
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


Возвращает количество полей в коллекции.

**Возвращает:**
int — количество полей в коллекции.
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


Возвращает объект перечислителя.

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




### remove(Field field) {#remove-com.aspose.words.Field-}
```
public void remove(Field field)
```


Удаляет указанное поле из этой коллекции и из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | Поле для удаления. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет поле с указанным индексом из этой коллекции и из документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

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
