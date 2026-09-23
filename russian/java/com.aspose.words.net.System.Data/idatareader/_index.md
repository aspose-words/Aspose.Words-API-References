---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words для Java"
description: "Предоставляет возможность чтения одного или нескольких потоков только для чтения наборов результатов, полученных выполнением команды в источнике данных, и реализуется поставщиками данных .NET Framework, которые работают с реляционными базами данных в Java."
type: docs
weight: 34
url: /ru/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Обеспечивает возможность чтения одного или нескольких потоков только для чтения наборов результатов, полученных выполнением команды в источнике данных, и реализуется поставщиками данных .NET Framework, которые работают с реляционными базами данных.
## Методы

| Метод | Описание |
| --- | --- |
| [close()](#close) | Закрывает объект [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [getDepth()](#getDepth) | Возвращает значение, указывающее глубину вложенности текущей строки. |
| [getRecordsAffected()](#getRecordsAffected) | Возвращает количество строк, изменённых, вставленных или удалённых в результате выполнения SQL‑оператора. |
| [getSchemaTable()](#getSchemaTable) | Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), описывающий метаданные столбцов [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | Возвращает значение, указывающее, закрыт ли data reader. |
| [nextResult()](#nextResult) | Перемещает data reader к следующему результату при чтении результатов пакетных SQL‑операторов. |
| [read()](#read) | Перемещает [IDataReader](../../com.aspose.words.net.system.data/idatareader/) к следующей записи. |
### close() {#close}
```
public abstract void close()
```


Закрывает объект [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Возвращает значение, указывающее глубину вложенности текущей строки.

**Returns:**
int — уровень вложенности.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Возвращает количество строк, изменённых, вставленных или удалённых в результате выполнения SQL‑оператора.

**Returns:**
int — количество изменённых, вставленных или удалённых строк; 0, если строки не затронуты или оператор завершился с ошибкой; и -1 для операторов SELECT.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Возвращает [DataTable](../../com.aspose.words.net.system.data/datatable/), описывающий метаданные столбцов [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Возвращает значение, указывающее, закрыт ли data reader.

**Returns:**
boolean — true, если data reader закрыт; иначе false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Перемещает data reader к следующему результату при чтении результатов пакетных SQL‑операторов.

**Returns:**
boolean — true, если есть дополнительные строки; иначе false.
### read() {#read}
```
public abstract boolean read()
```


Перемещает [IDataReader](../../com.aspose.words.net.system.data/idatareader/) к следующей записи.

**Returns:**
boolean — true, если есть дополнительные строки; иначе false.
