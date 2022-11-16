---
title: DataRowCollection
second_title: Справочник по API Aspose.Words для Java
description: Представляет набор строк для .
type: docs
weight: 21
url: /ru/java/com.aspose.words.net.system.data/datarowcollection/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

 Представляет набор строк для[DataTable](../../com.aspose.words.net.system.data/datatable).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow-) |  Добавляет указанный[DataRow](../../com.aspose.words.net.system.data/datarow) к[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) объект. |
| [add(Object[] values)](#add-java.lang.Object...-) |  Создает строку, используя указанные значения, и добавляет ее в[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection). |
| [clear()](#clear--) | Очищает коллекцию всех строк. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [find(Object[] keys)](#find-java.lang.Object---) | Получает строку, содержащую указанные значения первичного ключа. |
| [find(String primaryKeyValue)](#find-java.lang.String-) | Получает строку, заданную значением первичного ключа. |
| [get(int index)](#get-int-) | Получает строку по указанному индексу. |
| [get(Object[] values)](#get-java.lang.Object---) | Получает строку, содержащую указанные значения. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) |  Получает общее количество[DataRow](../../com.aspose.words.net.system.data/datarow) предметы из этой коллекции. |
| [hashCode()](#hashCode--) |  |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int-) | Вставляет новую строку в коллекцию в указанном месте. |
| [iterator()](#iterator--) | Получает java.util.Iterator для этой коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | Удаляет строку по указанному индексу из коллекции. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow-}
```
public void add(System.Data.DataRow row)
```


 Добавляет указанный[DataRow](../../com.aspose.words.net.system.data/datarow) к[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) объект.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | [DataRow](../../com.aspose.words.net.system.data/datarow) добавить. |

### add(Object[] values) {#add-java.lang.Object...-}
```
public void add(Object[] values)
```


 Создает строку, используя указанные значения, и добавляет ее в[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| values | java.lang.Object[] | Массив значений, которые используются для создания новой строки. |

### clear() {#clear--}
```
public void clear()
```


Очищает коллекцию всех строк.

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
### find(Object[] keys) {#find-java.lang.Object---}
```
public System.Data.DataRow find(Object[] keys)
```


Получает строку, содержащую указанные значения первичного ключа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| keys | java.lang.Object[] | Массив значений первичного ключа для поиска. Тип массива — Объект. |

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - А[DataRow](../../com.aspose.words.net.system.data/datarow) объект, содержащий указанные значения первичного ключа; в противном случае нулевое значение, если значение первичного ключа не существует в[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).
### find(String primaryKeyValue) {#find-java.lang.String-}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Получает строку, заданную значением первичного ключа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | Значение первичного ключа DataRow для поиска. |

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - DataRow, который содержит указанное значение первичного ключа; в противном случае нулевое значение, если значение первичного ключа не существует в DataRowCollection.
### get(int index) {#get-int-}
```
public System.Data.DataRow get(int index)
```


Получает строку по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Отсчитываемый от нуля индекс возвращаемой строки. |

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - указанный[DataRow](../../com.aspose.words.net.system.data/datarow).
### get(Object[] values) {#get-java.lang.Object---}
```
public System.Data.DataRow get(Object[] values)
```


Получает строку, содержащую указанные значения. Если присутствует столбец (столбцы) первичного ключа, будет использоваться индекс. Если индекса нет, то используется простое линейное сканирование. Будьте осторожны с этим, потому что это может занять значительное количество времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| values | java.lang.Object[] | данные строки |

**Возвращает:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - найденная строка или`null`
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


 Получает общее количество[DataRow](../../com.aspose.words.net.system.data/datarow) предметы из этой коллекции.

**Возвращает:**
 int - общее количество[DataRow](../../com.aspose.words.net.system.data/datarow) предметы из этой коллекции.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int-}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Вставляет новую строку в коллекцию в указанном месте.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | [DataRow](../../com.aspose.words.net.system.data/datarow) добавить. |
| pos | int | Расположение (отсчитываемое от нуля) в коллекции, куда вы хотите добавить DataRow. |

### iterator() {#iterator--}
```
public Iterator iterator()
```


Получает java.util.Iterator для этой коллекции.

**Возвращает:**
java.util.Iterator — java.util.Iterator для этой коллекции.
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


Удаляет строку по указанному индексу из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс удаляемой строки. |

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
