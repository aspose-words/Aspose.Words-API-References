---
title: FormFieldCollection
second_title: Справочник по API Aspose.Words для Java
description: Коллекция объектов FormField, представляющих все поля формы в диапазоне.
type: docs
weight: 297
url: /ru/java/com.aspose.words/formfieldcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class FormFieldCollection implements Iterable
```

 Коллекция**FormField** объекты, которые представляют все поля формы в диапазоне.

 Чтобы узнать больше, посетите**Working with Form Fields** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все поля формы из этой коллекции и из документа. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Возвращает поле формы по указанному индексу. |
| [get(String bookmarkName)](#get-java.lang.String-) | Возвращает поле формы по имени закладки. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Возвращает количество полей формы в коллекции. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Возвращает объект перечислителя. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String formField)](#remove-java.lang.String-) | Удаляет поле формы с указанным именем. |
| [removeAt(int index)](#removeAt-int-) | Удаляет поле формы по указанному индексу. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


Удаляет все поля формы из этой коллекции и из документа.

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
public FormField get(int index)
```


Возвращает поле формы по указанному индексу.

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс в коллекции. |

**Возвращает:**
[FormField](../../com.aspose.words/formfield) - Поле формы по указанному индексу.
### get(String bookmarkName) {#get-java.lang.String-}
```
public FormField get(String bookmarkName)
```


Возвращает поле формы по имени закладки. Возвращает null, если поле формы с указанным именем закладки не может быть найдено.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Имя закладки без учета регистра. |

**Возвращает:**
[FormField](../../com.aspose.words/formfield) - Поле формы по имени закладки.
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


Возвращает количество полей формы в коллекции.

**Возвращает:**
int - количество полей формы в коллекции.
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




### remove(String formField) {#remove-java.lang.String-}
```
public void remove(String formField)
```


Удаляет поле формы с указанным именем. Если есть закладка, связанная с полем формы, закладка не удаляется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| formField | java.lang.String | Нечувствительное к регистру имя удаляемого поля формы. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет поле формы по указанному индексу. Если есть закладка, связанная с полем формы, закладка не удаляется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс удаляемого поля формы. |

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
