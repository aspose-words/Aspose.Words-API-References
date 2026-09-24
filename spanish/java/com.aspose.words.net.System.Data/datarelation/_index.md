---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words para Java"
description: "Representa una relación padre/hijo entre dos objetos DataTable en Java."
type: docs
weight: 18
url: /es/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

Representa una relación padre/hijo entre dos objetos [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, las tablas padre e hijo, y matrices coincidentes de columnas padre e hijo. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, matrices coincidentes de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo, y un valor que indica si se deben crear restricciones. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo, y un valor que indica si se deben crear restricciones. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado, y los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo. |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Obtiene los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo de esta relación. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | Obtiene el [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) de la relación. |
| [getChildTable()](#getChildTable) | Obtiene la tabla hija de esta relación. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | Obtiene el [DataSet](../../com.aspose.words.net.system.data/dataset/) al que pertenece el [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Obtiene una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que son las columnas padre de este [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Obtiene el [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) que garantiza que los valores en la columna padre de un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sean únicos. |
| [getParentTable()](#getParentTable) | Obtiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) padre de este [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | Obtiene el nombre usado para recuperar un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) de la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | Establece un valor que indica si los objetos [DataRelation](../../com.aspose.words.net.system.data/datarelation/) están anidados. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, las tablas padre e hijo, y matrices coincidentes de columnas padre e hijo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relationName | java.lang.String | El nombre del DataRelation. Si es nulo o una cadena vacía (\"\"), se asignará un nombre predeterminado cuando el objeto creado se añada a la DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla padre en la relación. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | La tabla hija en la relación. |
| parentColumnNames | java.lang.String[] | El nombre de la DataColumn padre en la relación. |
| childColumnNames | java.lang.String[] | Los DataColumn hijos en la relación. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, matrices coincidentes de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo, y un valor que indica si se deben crear restricciones.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relationName | java.lang.String | El nombre de la relación. Si es nulo o una cadena vacía (""), se asignará un nombre predeterminado cuando el objeto creado se añada a la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo. |
| createConstraints | boolean | Un valor que indica si se deben crear restricciones. true, si se crean restricciones. De lo contrario, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre especificado, los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo, y un valor que indica si se deben crear restricciones.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relationName | java.lang.String | El nombre de la relación. Si es nulo o una cadena vacía (""), se asignará un nombre predeterminado cuando el objeto creado se añada a la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre en la relación. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo en la relación. |
| createConstraints | boolean | Un valor que indica si se crean restricciones. true, si se crean restricciones. De lo contrario, false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inicializa una nueva instancia de la clase [DataRelation](../../com.aspose.words.net.system.data/datarelation/) usando el nombre [DataRelation](../../com.aspose.words.net.system.data/datarelation/) especificado, y los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre e hijo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| relationName | java.lang.String | El nombre del [DataRelation](../../com.aspose.words.net.system.data/datarelation/). Si es nulo o una cadena vacía (""), se asignará un nombre predeterminado cuando el objeto creado se añada a la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre en la relación. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo en la relación. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - los nombres de DataColumn hijos de esta relación.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Obtiene los objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo de esta relación.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getChildKey() {#getChildKey}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getChildKeyConstraint() {#getChildKeyConstraint}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


Obtiene el [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) de la relación.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Obtiene la tabla hija de esta relación.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - el nombre de la DataTable hija de este DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Obtiene el [DataSet](../../com.aspose.words.net.system.data/dataset/) al que pertenece el [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - los nombres de DataColumn padre de esta relación.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Obtiene una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que son las columnas padre de este [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que son las columnas padre de este [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### getParentKey() {#getParentKey}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getParentKeyConstraint() {#getParentKeyConstraint}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


Obtiene el [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) que garantiza que los valores en la columna padre de un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sean únicos.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Obtiene la [DataTable](../../com.aspose.words.net.system.data/datatable/) padre de este [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - el nombre de la DataTable padre de este DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


Obtiene el nombre usado para recuperar un [DataRelation](../../com.aspose.words.net.system.data/datarelation/) de la [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Returns:**
java.lang.String - El nombre de un [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


Establece un valor que indica si los objetos [DataRelation](../../com.aspose.words.net.system.data/datarelation/) están anidados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | true, si los objetos [DataRelation](../../com.aspose.words.net.system.data/datarelation/) están anidados; de lo contrario, false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

