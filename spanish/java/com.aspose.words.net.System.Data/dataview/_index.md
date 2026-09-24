---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words para Java"
description: "Representa una vista personalizada vinculable a datos de un DataTable para ordenar, filtrar, buscar, editar y navegar en Java."
type: docs
weight: 28
url: /es/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Representa una vista personalizada, vinculable a datos, de un [DataTable](../../com.aspose.words.net.system.data/datatable/) para ordenar, filtrar, buscar, editar y navegar.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Inicializa una nueva instancia de la clase [DataView](../../com.aspose.words.net.system.data/dataview/) con el [DataTable](../../com.aspose.words.net.system.data/datatable/) especificado. |
## Métodos

| Método | Descripción |
| --- | --- |
| [close()](#close) | Cierra el [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | Obtiene una fila de datos de una tabla especificada. |
| [getCount()](#getCount) | Obtiene el número de registros en el [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | Obtiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) de origen. |
| [iterator()](#iterator) | Obtiene un enumerador para este [DataView](../../com.aspose.words.net.system.data/dataview/). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Inicializa una nueva instancia de la clase [DataView](../../com.aspose.words.net.system.data/dataview/) con el [DataTable](../../com.aspose.words.net.system.data/datatable/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Una [DataTable](../../com.aspose.words.net.system.data/datatable/) para agregar al [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


Cierra el [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Obtiene una fila de datos de una tabla especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| recordIndex | int | El índice de un registro en la [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de registros en el [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - El número de registros en el [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) de origen.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Obtiene un enumerador para este [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - Un java.util.Iterator para navegar por la lista.
