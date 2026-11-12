---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию строк для DataTable в Java."
type: docs
weight: 21
url: /ru/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Представляет коллекцию строк для [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Методы

| Метод | Описание |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Добавляет указанный [DataRow](../../com.aspose.words.net.system.data/datarow/) в объект [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [add(Object[] values)](#add-java.lang.Object...) | Создаёт строку, используя указанные значения, и добавляет её в [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | Очищает коллекцию от всех строк. |
| [find(Object[] keys)](#find-java.lang.Object) | Получает строку, содержащую указанные значения первичного ключа. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Получает строку, указанную значением первичного ключа. |
| [get(int index)](#get-int) | Получает строку по указанному индексу. |
| [get(Object[] values)](#get-java.lang.Object) | Получает строку, содержащую указанные значения. |
| [getCount()](#getCount) | Получает общее количество объектов [DataRow](../../com.aspose.words.net.system.data/datarow/) в этой коллекции. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Вставляет новую строку в коллекцию в указанное место. |
| [iterator()](#iterator) | Получает java.util.Iterator для этой коллекции. |
| [removeAt(int index)](#removeAt-int) | Удаляет строку по указанному индексу из коллекции. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Добавляет указанный [DataRow](../../com.aspose.words.net.system.data/datarow/) в объект [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Элемент [DataRow](../../com.aspose.words.net.system.data/datarow/) для добавления. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Создаёт строку, используя указанные значения, и добавляет её в [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значения | java.lang.Object[] | Массив значений, используемых для создания новой строки. |

### clear() {#clear}
```
public void clear()
```


Очищает коллекцию от всех строк.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Получает строку, содержащую указанные значения первичного ключа.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключи | java.lang.Object[] | Массив значений первичного ключа для поиска. Тип массива — Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Получает строку, указанную значением первичного ключа.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | Значение первичного ключа DataRow для поиска. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Получает строку по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс строки, которую нужно вернуть. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Получает строку, содержащую указанные значения. Если присутствуют столбцы первичного ключа, будет использован индекс. Если индекса нет, будет выполнено простое линейное сканирование. Будьте осторожны, так как это может занять значительное время.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значения | java.lang.Object[] | данные строки |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Получает общее количество объектов [DataRow](../../com.aspose.words.net.system.data/datarow/) в этой коллекции.

**Returns:**
int - Общее количество объектов [DataRow](../../com.aspose.words.net.system.data/datarow/) в этой коллекции.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Вставляет новую строку в коллекцию в указанное место.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Элемент [DataRow](../../com.aspose.words.net.system.data/datarow/) для добавления. |
| pos | int | Расположение (ноль‑базовое) в коллекции, в которое вы хотите добавить DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Получает java.util.Iterator для этой коллекции.

**Returns:**
java.util.Iterator - Итератор java.util.Iterator для этой коллекции.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет строку по указанному индексу из коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс строки, которую нужно удалить. |

