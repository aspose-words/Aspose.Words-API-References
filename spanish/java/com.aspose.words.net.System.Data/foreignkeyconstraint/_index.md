---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words para Java"
description: "Representa una restricción de acción aplicada a un conjunto de columnas en una relación de clave primaria/clave externa cuando un valor o fila se elimina o actualiza en Java."
type: docs
weight: 29
url: /es/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Representa una restricción de acción aplicada a un conjunto de columnas en una relación clave primaria/clave externa cuando un valor o fila se elimina o actualiza.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con el nombre especificado y matrices de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con los [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo especificados. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con el nombre, los [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo especificados. |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Obtiene un valor que indica si el [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) actual es idéntico al objeto especificado. |
| [getColumns()](#getColumns) | Obtiene las columnas hijo de esta restricción. |
| [getConstraintName()](#getConstraintName) | El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | Obtiene la acción que ocurre en esta restricción cuando se elimina una fila. |
| [getRelatedColumns()](#getRelatedColumns) | Las columnas padre de esta restricción. |
| [getRelatedTable()](#getRelatedTable) | Obtiene la tabla padre de esta restricción. |
| [getTable()](#getTable) | Obtiene la tabla hijo de esta restricción. |
| [getUpdateRule()](#getUpdateRule) | Obtiene la acción que ocurre en esta restricción cuando se actualiza una fila. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con el nombre especificado y matrices de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| constraintName | java.lang.String | El nombre del [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Si es nulo o una cadena vacía, se asignará un nombre predeterminado al agregarlo a la colección de restricciones. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre en la restricción. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Una matriz de [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo en la restricción. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con los [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre en la restricción. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo en la restricción. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Inicializa una nueva instancia de la clase [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) con el nombre, los [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre y hijo especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| constraintName | java.lang.String | El nombre de la restricción. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) padre en la restricción. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | El [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) hijo en la restricción. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Obtiene un valor que indica si el [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) actual es idéntico al objeto especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | java.lang.Object | El objeto con el que se compara este [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). Dos [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) son iguales si restringen las mismas columnas. |

**Returns:**
boolean - true, si los objetos son idénticos; de lo contrario, false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Obtiene las columnas hijo de esta restricción.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que son las columnas hijo de la restricción.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - El nombre del [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Obtiene la acción que ocurre en esta restricción cuando se elimina una fila.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Las columnas padre de esta restricción.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Una matriz de objetos [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) que son las columnas padre de la restricción.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Obtiene la tabla padre de esta restricción.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtiene la tabla hijo de esta restricción.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Obtiene la acción que ocurre en esta restricción cuando se actualiza una fila.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


El nombre de una restricción en la [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El nombre del [Constraint](../../com.aspose.words.net.system.data/constraint/). |

