---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words para Java"
description: "Representa una tabla de datos en memoria en Java."
type: docs
weight: 25
url: /es/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Representa una tabla de datos en memoria.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataTable()](#DataTable) | Inicializa una nueva instancia de la clase [DataTable](../../com.aspose.words.net.system.data/datatable/) sin argumentos. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Inicializa una nueva instancia de la clase [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre de tabla especificado. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Crea un objeto envolviendo el ResultSet especificado. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Crea un objeto envolviendo el ResultSet especificado. |
## Métodos

| Método | Descripción |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Confirma todos los cambios realizados en esta tabla desde la última vez que se llamó a [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges). |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Comprueba si la columna dada existe o no. |
| [getChildRelations()](#getChildRelations) | Obtiene la colección de relaciones secundarias para este [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | Análogo para .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Obtiene la colección de columnas que pertenecen a esta tabla. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Obtiene la colección de restricciones mantenidas por esta tabla. |
| [getDataSet()](#getDataSet) | Obtiene el [DataSet](../../com.aspose.words.net.system.data/dataset/) al que pertenece esta tabla. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Obtiene el espacio de nombres para la representación XML de los datos almacenados en el [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getParentRelations()](#getParentRelations) | Obtiene la colección de relaciones principales para este [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | Obtiene una matriz de columnas que funcionan como claves primarias para la tabla de datos. |
| [getResultSet()](#getResultSet) | Devuelve el objeto ResultSet de Java subyacente. |
| [getRows()](#getRows) | Obtiene la colección de filas que pertenecen a esta tabla. |
| [getTableName()](#getTableName) | Obtiene el nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | Crea un nuevo [DataRow](../../com.aspose.words.net.system.data/datarow/) con el mismo esquema que la tabla. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Recarga todos los datos del ResultSet si está presente. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Establece el espacio de nombres para la representación XML de los datos almacenados en el [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Establece una matriz de columnas que funcionan como claves primarias para la tabla de datos. |
| [setTableName(String value)](#setTableName-java.lang.String) | Establece el nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


Inicializa una nueva instancia de la clase [DataTable](../../com.aspose.words.net.system.data/datatable/) sin argumentos.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Inicializa una nueva instancia de la clase [DataTable](../../com.aspose.words.net.system.data/datatable/) con el nombre de tabla especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableName | java.lang.String | El nombre que se asignará a la tabla. Si  tableName  es nulo o una cadena vacía, se asigna un nombre predeterminado al agregarla a la [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Crea un objeto envolviendo el ResultSet especificado. Intenta obtener el nombre de la tabla a partir de los metadatos de la primera columna del ResultSet.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | conjunto de datos |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Crea un objeto envolviendo el ResultSet especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | conjunto de datos |
| tableName | java.lang.String | nombre de la tabla |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Confirma todos los cambios realizados en esta tabla desde la última vez que se llamó a [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges).

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Comprueba si la columna dada existe o no.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columnName | java.lang.String | nombre de la columna |

**Returns:**
booleano - `true` indica que la columna puede encontrarse mediante el `columnName` dado
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Obtiene la colección de relaciones secundarias para este [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Análogo para .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | - índice de la columna |

**Returns:**
java.lang.String - nombre de la columna por su índice.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Obtiene la colección de columnas que pertenecen a esta tabla.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - recuento de columnas
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Obtiene la colección de restricciones mantenidas por esta tabla.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Obtiene el [DataSet](../../com.aspose.words.net.system.data/dataset/) al que pertenece esta tabla.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - bandera que indica si hay violación de restricción de comprobación o no
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtiene el espacio de nombres para la representación XML de los datos almacenados en el [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - El espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Obtiene la colección de relaciones principales para este [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Obtiene una matriz de columnas que funcionan como claves primarias para la tabla de datos.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Devuelve el objeto Java ResultSet subyacente. Idealmente nos gustaría trabajar con DataTable al estilo .Net. Pero algunos usuarios e incluso parte de nuestro código de ejemplo están usando esta propiedad.

**Returns:**
java.sql.ResultSet - el java.sql.ResultSet subyacente
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Obtiene la colección de filas que pertenecen a esta tabla.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Obtiene el nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - El nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Crea un nuevo [DataRow](../../com.aspose.words.net.system.data/datarow/) con el mismo esquema que la tabla.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


Actualizar listener cuando DataColumn eliminado

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


Actualizar listener cuando DataColumn insertado

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


Actualizar listener cuando DataRow cambiado

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


Actualizar listener cuando DataRow eliminado

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


Actualizar el escuchador cuando se inserta DataRow

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


Recarga todos los datos del ResultSet si está presente.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| enforceConstraints | boolean | es la bandera que indica si hay violación de restricción de comprobación o no |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Establece el espacio de nombres para la representación XML de los datos almacenados en el [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El espacio de nombres del [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Establece una matriz de columnas que funcionan como claves primarias para la tabla de datos.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Establece el nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El nombre del [DataTable](../../com.aspose.words.net.system.data/datatable/). |

