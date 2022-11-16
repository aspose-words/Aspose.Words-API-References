---
title: IDataReader
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет средство для чтения одного или нескольких потоков наборов результатов только для прямого доступа, полученных путем выполнения команды в источнике данных, и реализуется поставщиками данных .NET Framework, которые обращаются к реляционным базам данных.
type: docs
weight: 34
url: /ru/java/com.aspose.words.net.system.data/idatareader/
---

**Все реализованные интерфейсы:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
```
public interface IDataReader extends System.Data.IDataRecord
```

Предоставляет средство для чтения одного или нескольких потоков наборов результатов, доступных только в прямом направлении, полученных путем выполнения команды в источнике данных, и реализуется поставщиками данных .NET Framework, которые обращаются к реляционным базам данных.
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close--) |  Закрывает[IDataReader](../../com.aspose.words.net.system.data/idatareader) Объект. |
| [getDepth()](#getDepth--) | Получает значение, указывающее глубину вложенности для текущей строки. |
| [getRecordsAffected()](#getRecordsAffected--) | Получает количество строк, измененных, вставленных или удаленных при выполнении инструкции SQL. |
| [getSchemaTable()](#getSchemaTable--) |  Возвращает[DataTable](../../com.aspose.words.net.system.data/datatable) который описывает метаданные столбца[IDataReader](../../com.aspose.words.net.system.data/idatareader). |
| [isClosed()](#isClosed--) | Получает значение, указывающее, закрыто ли средство чтения данных. |
| [nextResult()](#nextResult--) | Переводит средство чтения данных к следующему результату при чтении результатов пакетных операторов SQL. |
| [read()](#read--) |  продвигает[IDataReader](../../com.aspose.words.net.system.data/idatareader) к следующей записи. |
### close() {#close--}
```
public abstract void close()
```


 Закрывает[IDataReader](../../com.aspose.words.net.system.data/idatareader) Объект.

### getDepth() {#getDepth--}
```
public abstract int getDepth()
```


Получает значение, указывающее глубину вложенности для текущей строки.

**Возвращает:**
int - Уровень вложенности.
### getRecordsAffected() {#getRecordsAffected--}
```
public abstract int getRecordsAffected()
```


Получает количество строк, измененных, вставленных или удаленных при выполнении инструкции SQL.

**Возвращает:**
int — количество измененных, вставленных или удаленных строк; 0, если ни одна строка не была затронута или оператор завершился ошибкой; и -1 для операторов SELECT.
### getSchemaTable() {#getSchemaTable--}
```
public abstract System.Data.DataTable getSchemaTable()
```


 Возвращает[DataTable](../../com.aspose.words.net.system.data/datatable) который описывает метаданные столбца[IDataReader](../../com.aspose.words.net.system.data/idatareader).

**Возвращает:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - А[DataTable](../../com.aspose.words.net.system.data/datatable)который описывает метаданные столбца.
### isClosed() {#isClosed--}
```
public abstract boolean isClosed()
```


Получает значение, указывающее, закрыто ли средство чтения данных.

**Возвращает:**
boolean - true, если считыватель данных закрыт; в противном случае ложно.
### nextResult() {#nextResult--}
```
public abstract boolean nextResult()
```


Переводит средство чтения данных к следующему результату при чтении результатов пакетных операторов SQL.

**Возвращает:**
boolean - true, если строк больше; в противном случае ложно.
### read() {#read--}
```
public abstract boolean read()
```


 продвигает[IDataReader](../../com.aspose.words.net.system.data/idatareader) к следующей записи.

**Возвращает:**
boolean - true, если строк больше; в противном случае ложно.