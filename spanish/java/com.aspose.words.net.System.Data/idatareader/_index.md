---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words para Java"
description: "Proporciona un medio para leer uno o más flujos de solo avance de conjuntos de resultados obtenidos al ejecutar un comando en una fuente de datos y es implementado por los proveedores de datos del .NET Framework que acceden a bases de datos relacionales en Java."
type: docs
weight: 34
url: /es/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Proporciona un medio para leer uno o más flujos solo de avance de conjuntos de resultados obtenidos al ejecutar un comando en una fuente de datos, y es implementado por los proveedores de datos del .NET Framework que acceden a bases de datos relacionales.
## Métodos

| Método | Descripción |
| --- | --- |
| [close()](#close) | Cierra el objeto [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [getDepth()](#getDepth) | Obtiene un valor que indica la profundidad de anidamiento para la fila actual. |
| [getRecordsAffected()](#getRecordsAffected) | Obtiene el número de filas modificadas, insertadas o eliminadas por la ejecución de la sentencia SQL. |
| [getSchemaTable()](#getSchemaTable) | Devuelve una [DataTable](../../com.aspose.words.net.system.data/datatable/) que describe los metadatos de columna del [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | Obtiene un valor que indica si el lector de datos está cerrado. |
| [nextResult()](#nextResult) | Avanza el lector de datos al siguiente resultado, al leer los resultados de sentencias SQL por lotes. |
| [read()](#read) | Avanza el [IDataReader](../../com.aspose.words.net.system.data/idatareader/) al siguiente registro. |
### close() {#close}
```
public abstract void close()
```


Cierra el objeto [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Obtiene un valor que indica la profundidad de anidamiento para la fila actual.

**Returns:**
int - El nivel de anidamiento.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Obtiene el número de filas modificadas, insertadas o eliminadas por la ejecución de la sentencia SQL.

**Returns:**
int - El número de filas modificadas, insertadas o eliminadas; 0 si no se afectó ninguna fila o la sentencia falló; y -1 para sentencias SELECT.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Devuelve una [DataTable](../../com.aspose.words.net.system.data/datatable/) que describe los metadatos de columna del [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Obtiene un valor que indica si el lector de datos está cerrado.

**Returns:**
boolean - true si el lector de datos está cerrado; de lo contrario, false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Avanza el lector de datos al siguiente resultado, al leer los resultados de sentencias SQL por lotes.

**Returns:**
boolean - true si hay más filas; de lo contrario, false.
### read() {#read}
```
public abstract boolean read()
```


Avanza el [IDataReader](../../com.aspose.words.net.system.data/idatareader/) al siguiente registro.

**Returns:**
boolean - true si hay más filas; de lo contrario, false.
