---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words para Java"
description: "Representa una restricción en un conjunto de columnas en el que todos los valores deben ser únicos en Java."
type: docs
weight: 32
url: /es/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Representa una restricción en un conjunto de columnas en el que todos los valores deben ser únicos.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con el nombre especificado, una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir y un valor que indica si la restricción es una clave primaria. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir y un valor que indica si la restricción es una clave primaria. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con la matriz dada de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado. |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Compara esta restricción con una segunda para determinar si ambas son idénticas. |
| [getColumns()](#getColumns) | Obtiene la matriz de columnas que afecta esta restricción. |
| [getConstraintName()](#getConstraintName) | El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | Obtiene la tabla a la que pertenece esta restricción. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Obtiene un valor que indica si la restricción está en una clave primaria o no. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con el nombre especificado, una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir y un valor que indica si la restricción es una clave primaria.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la restricción. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir. |
| isPrimaryKey | boolean | verdadero para indicar que la restricción es una clave primaria; de lo contrario, falso. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir y un valor que indica si la restricción es una clave primaria.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir. |
| isPrimaryKey | boolean | verdadero para indicar que la restricción es una clave primaria; de lo contrario, falso. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con la matriz dada de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | La matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Inicializa una nueva instancia de la clase [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) con el [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) a restringir. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Compara esta restricción con una segunda para determinar si ambas son idénticas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key2 | java.lang.Object | El objeto con el que se compara este [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/). |

**Returns:**
boolean - verdadero, si las restricciones son iguales; de lo contrario, falso.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Obtiene la matriz de columnas que afecta esta restricción.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - El nombre del [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtiene la tabla a la que pertenece esta restricción.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the constraint belongs.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isPrimaryKey() {#isPrimaryKey}
```
public boolean isPrimaryKey()
```


Obtiene un valor que indica si la restricción está en una clave primaria o no.

**Returns:**
boolean - verdadero, si la restricción está en una clave primaria; de lo contrario, falso.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El nombre del [Constraint](../../com.aspose.words.net.system.data/constraint/). |

