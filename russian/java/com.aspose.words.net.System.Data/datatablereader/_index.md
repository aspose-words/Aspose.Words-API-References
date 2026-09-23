---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words для Java"
description: "DataTableReader получает содержимое одного или нескольких объектов DataTable в виде одного или нескольких только для чтения, только вперёд перемещаемых наборов результатов в Java."
type: docs
weight: 27
url: /ru/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) получает содержимое одного или нескольких [DataTable](../../com.aspose.words.net.system.data/datatable/) объектов в виде одного или нескольких только для чтения, только вперёд перемещаемых наборов результатов.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Инициализирует новый экземпляр класса [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) , используя данные из предоставленного [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Инициализирует новый экземпляр класса [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) с использованием предоставленного массива объектов [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close) | Закрывает текущий [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [get(int ordinal)](#get-int) | Получает значение указанного столбца в его исходном формате по порядковому номеру столбца. |
| [get(String name)](#get-java.lang.String) | Получает значение указанного столбца в его исходном формате по имени столбца. |
| [getDepth()](#getDepth) | Глубина вложенности текущей строки [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | Возвращает количество столбцов в текущей строке. |
| [getFieldType(int ordinal)](#getFieldType-int) | Получает java.lang.Class, который является типом данных объекта. |
| [getName(int ordinal)](#getName-int) | Получает значение указанного столбца как java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected) | Получает количество строк, вставленных, изменённых или удалённых в результате выполнения SQL‑запроса. |
| [getSchemaTable()](#getSchemaTable) | Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), который описывает метаданные столбцов [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getValue(int ordinal)](#getValue-int) | Получает значение указанного столбца в его исходном формате. |
| [hasRows()](#hasRows) | Получает значение, указывающее, содержит ли [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) одну или более строк. |
| [isClosed()](#isClosed) | Получает значение, указывающее, закрыт ли [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [iterator()](#iterator) | Возвращает перечислитель, который можно использовать для перебора элементов коллекции. |
| [nextResult()](#nextResult) | Перемещает [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) к следующему набору результатов, если он существует. |
| [read()](#read) | Перемещает [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) к следующей записи. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Инициализирует новый экземпляр класса [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) , используя данные из предоставленного [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Таблица [DataTable](../../com.aspose.words.net.system.data/datatable/), из которой новый [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) получает свой набор результатов. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Инициализирует новый экземпляр класса [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) с использованием предоставленного массива объектов [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | Массив объектов [DataTable](../../com.aspose.words.net.system.data/datatable/) который предоставляет результаты для нового объекта [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |

### close() {#close}
```
public void close()
```


Закрывает текущий [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Получает значение указанного столбца в его исходном формате по порядковому номеру столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| порядковый | int | Порядковый номер столбца, начинающийся с нуля. |

**Returns:**
java.lang.Object — Значение указанного столбца в его исходном формате.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Получает значение указанного столбца в его исходном формате по имени столбца.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя столбца. |

**Returns:**
java.lang.Object — Значение указанного столбца в его исходном формате.
### getDepth() {#getDepth}
```
public int getDepth()
```


Глубина вложенности текущей строки [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int — Глубина вложенности текущей строки; всегда ноль.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Возвращает количество столбцов в текущей строке.

**Returns:**
int — Когда не находится в действительном наборе результатов, 0; в противном случае количество столбцов в текущей строке.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Получает java.lang.Class, который является типом данных объекта.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| порядковый | int | Порядковый номер столбца, начинающийся с нуля. |

**Returns:**
java.lang.Class — java.lang.Class, который является типом данных объекта.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Получает значение указанного столбца как java.lang.String.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| порядковый | int | Порядковый номер столбца, начинающийся с нуля |

**Returns:**
java.lang.String - Имя указанного столбца.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


Получает количество строк, вставленных, изменённых или удалённых в результате выполнения SQL‑запроса.

**Returns:**
int - [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) не поддерживает это свойство и всегда возвращает 0.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), который описывает метаданные столбцов [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Получает значение указанного столбца в его исходном формате.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| порядковый | int | Порядковый номер столбца, начинающийся с нуля |

**Returns:**
java.lang.Object - Значение указанного столбца. Этот метод возвращает DBNull для столбцов со значением null.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


Получает значение, указывающее, содержит ли [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) одну или более строк.

**Returns:**
boolean - true, если [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) содержит одну или более строк; иначе false.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


Получает значение, указывающее, закрыт ли [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
boolean - Возвращает true, если [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) закрыт; иначе false.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает перечислитель, который можно использовать для перебора элементов коллекции.

**Returns:**
java.util.Iterator - Объект java.util.Iterator, представляющий коллекцию элементов.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


Перемещает [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) к следующему набору результатов, если он существует.

**Returns:**
boolean - true, если существует другой набор результатов; иначе false.
### read() {#read}
```
public boolean read()
```


Перемещает [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) к следующей записи.

**Returns:**
boolean - true, если есть следующая строка для чтения; иначе false.
