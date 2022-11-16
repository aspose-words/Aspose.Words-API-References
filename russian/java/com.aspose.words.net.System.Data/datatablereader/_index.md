---
title: DataTableReader
second_title: Справочник по API Aspose.Words для Java
description: Получает содержимое одного или нескольких объектов в виде одного или нескольких наборов результатов только для чтения и только для прямого доступа.
type: docs
weight: 27
url: /ru/java/com.aspose.words.net.system.data/datatablereader/
---

**Наследование:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) получает содержимое одного или нескольких[DataTable](../../com.aspose.words.net.system.data/datatable) объекты в виде одного или нескольких наборов результатов только для чтения и только для пересылки.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable-) |  Инициализирует новый экземпляр[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) класс, используя данные из предоставленного[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable---) |  Инициализирует новый экземпляр[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) класс, используя предоставленный массив[DataTable](../../com.aspose.words.net.system.data/datatable) объекты. |
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close--) |  Закрывает текущий[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int ordinal)](#get-int-) | Получает значение указанного столбца в его собственном формате с учетом порядкового номера столбца. |
| [get(String name)](#get-java.lang.String-) | Получает значение указанного столбца в его собственном формате с учетом имени столбца. |
| [getClass()](#getClass--) |  |
| [getDepth()](#getDepth--) |  Глубина вложенности текущей строки[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [getFieldCount()](#getFieldCount--) | Возвращает количество столбцов в текущей строке. |
| [getFieldType(int ordinal)](#getFieldType-int-) | Получает java.lang.Class, являющийся типом данных объекта. |
| [getName(int ordinal)](#getName-int-) | Получает значение указанного столбца в виде java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected--) | Получает количество строк, вставленных, измененных или удаленных при выполнении инструкции SQL. |
| [getSchemaTable()](#getSchemaTable--) |  Возвращает[DataTable](../../com.aspose.words.net.system.data/datatable) который описывает метаданные столбца[DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [getValue(int ordinal)](#getValue-int-) | Получает значение указанного столбца в его собственном формате. |
| [hasRows()](#hasRows--) |  Получает значение, указывающее, является ли[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) содержит одну или несколько строк. |
| [hashCode()](#hashCode--) |  |
| [isClosed()](#isClosed--) |  Получает значение, указывающее, является ли[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) закрыто. |
| [iterator()](#iterator--) | Возвращает перечислитель, который можно использовать для перебора коллекции элементов. |
| [nextResult()](#nextResult--) |  продвигает[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) к следующему набору результатов, если таковой имеется. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [read()](#read--) |  продвигает[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) к следующей записи. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable-}
```
public DataTableReader(System.Data.DataTable dataTable)
```


 Инициализирует новый экземпляр[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) класс, используя данные из предоставленного[DataTable](../../com.aspose.words.net.system.data/datatable).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | [DataTable](../../com.aspose.words.net.system.data/datatable) из чего новый[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) получает свой результирующий набор. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable---}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


 Инициализирует новый экземпляр[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) класс, используя предоставленный массив[DataTable](../../com.aspose.words.net.system.data/datatable) объекты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable) |  Массив[DataTable](../../com.aspose.words.net.system.data/datatable) объекты, которые предоставляют результаты для нового[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) объект. |

### close() {#close--}
```
public void close()
```


 Закрывает текущий[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

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
### get(int ordinal) {#get-int-}
```
public Object get(int ordinal)
```


Получает значение указанного столбца в его собственном формате с учетом порядкового номера столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ordinal | int | Порядковый номер столбца с отсчетом от нуля. |

**Возвращает:**
java.lang.Object — значение указанного столбца в его собственном формате.
### get(String name) {#get-java.lang.String-}
```
public Object get(String name)
```


Получает значение указанного столбца в его собственном формате с учетом имени столбца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя столбца. |

**Возвращает:**
java.lang.Object — значение указанного столбца в его собственном формате.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDepth() {#getDepth--}
```
public int getDepth()
```


 Глубина вложенности текущей строки[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**Возвращает:**
int - глубина вложенности текущей строки; всегда ноль.
### getFieldCount() {#getFieldCount--}
```
public int getFieldCount()
```


Возвращает количество столбцов в текущей строке.

**Возвращает:**
int — если не находится в допустимом результирующем наборе, 0; в противном случае количество столбцов в текущей строке.
### getFieldType(int ordinal) {#getFieldType-int-}
```
public Class getFieldType(int ordinal)
```


Получает java.lang.Class, являющийся типом данных объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ordinal | int | Порядковый номер столбца с отсчетом от нуля. |

**Возвращает:**
java.lang.Class — java.lang.Class, являющийся типом данных объекта.
### getName(int ordinal) {#getName-int-}
```
public String getName(int ordinal)
```


Получает значение указанного столбца в виде java.lang.String.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ordinal | int | Порядковый номер столбца с отсчетом от нуля |

**Возвращает:**
java.lang.String — имя указанного столбца.
### getRecordsAffected() {#getRecordsAffected--}
```
public int getRecordsAffected()
```


Получает количество строк, вставленных, измененных или удаленных при выполнении инструкции SQL.

**Возвращает:**
 интервал -[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) не поддерживает это свойство и всегда возвращает 0.
### getSchemaTable() {#getSchemaTable--}
```
public System.Data.DataTable getSchemaTable()
```


 Возвращает[DataTable](../../com.aspose.words.net.system.data/datatable) который описывает метаданные столбца[DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable)который описывает метаданные столбца.
### getValue(int ordinal) {#getValue-int-}
```
public Object getValue(int ordinal)
```


Получает значение указанного столбца в его собственном формате.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ordinal | int | Порядковый номер столбца с отсчетом от нуля |

**Возвращает:**
java.lang.Object — значение указанного столбца. Этот метод возвращает значение DBNull для нулевых столбцов.
### hasRows() {#hasRows--}
```
public boolean hasRows()
```


 Получает значение, указывающее, является ли[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) содержит одну или несколько строк.

**Возвращает:**
 boolean - истина, если[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) содержит одну или несколько строк; иначе ложно.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isClosed() {#isClosed--}
```
public boolean isClosed()
```


 Получает значение, указывающее, является ли[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) закрыто.

**Возвращает:**
 boolean — возвращает true, если[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) закрыто; в противном случае ложно.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает перечислитель, который можно использовать для перебора коллекции элементов.

**Возвращает:**
java.util.Iterator — объект java.util.Iterator, представляющий коллекцию элементов.
### nextResult() {#nextResult--}
```
public boolean nextResult()
```


 продвигает[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) к следующему набору результатов, если таковой имеется.

**Возвращает:**
boolean - true, если был другой результирующий набор; иначе ложно.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### read() {#read--}
```
public boolean read()
```


 продвигает[DataTableReader](../../com.aspose.words.net.system.data/datatablereader) к следующей записи.

**Возвращает:**
boolean - true, если есть еще одна строка для чтения; иначе ложно.
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
