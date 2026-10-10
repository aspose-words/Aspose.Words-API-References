---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words pour Java"
description: "Représente le schéma d'une colonne dans un DataTable en Java."
type: docs
weight: 14
url: /fr/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Représente le schéma d'une colonne dans un [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Constructors

| Constructor | Description |
| --- | --- |
| [DataColumn()](#DataColumn) | Initialise une nouvelle instance d'une classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de type chaîne. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de type chaîne, en utilisant le nom de colonne spécifié. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Initialise une nouvelle instance de la classe @\{link DataColumn\} en utilisant le nom de colonne spécifié et la table à laquelle elle appartient. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) en utilisant le nom de colonne spécifié et le type de données. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) en utilisant le nom de colonne spécifié, le type de données et le tableau de données auquel elle appartient. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Obtient une valeur qui indique si les valeurs null sont autorisées dans cette colonne pour les lignes appartenant au tableau. |
| [getAutoIncrement()](#getAutoIncrement) | Obtient une valeur qui indique si la colonne incrémente automatiquement la valeur de la colonne pour les nouvelles lignes ajoutées à la table. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Obtient la valeur de départ d'une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Obtient l'incrément utilisé par une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true. |
| [getCaption()](#getCaption) | Obtient la légende de la colonne. |
| [getColumnMapping()](#getColumnMapping) | Obtient le [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la colonne. |
| [getColumnName()](#getColumnName) | Obtient le nom de la colonne dans le [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | Obtient le type de données stockées dans la colonne. |
| [getDefaultValue()](#getDefaultValue) | Obtient la valeur par défaut de la colonne lors de la création de nouvelles lignes. |
| [getExpression()](#getExpression) | Obtient l'expression utilisée pour filtrer les lignes, calculer les valeurs d'une colonne ou créer une colonne agrégée. |
| [getMaxLength()](#getMaxLength) | Obtient la longueur maximale d'une colonne texte. |
| [getNamespace()](#getNamespace) | Obtient l'espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | Obtient la position de la colonne dans la collection [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getPrefix()](#getPrefix) | Obtient un préfixe XML qui alias l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | Obtient une valeur qui indique si la colonne autorise les modifications dès qu'une ligne a été ajoutée à la table. |
| [getTable()](#getTable) | Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) auquel la colonne appartient. |
| [getUnique()](#getUnique) | Obtient une valeur qui indique si les valeurs de chaque ligne de la colonne doivent être uniques. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Définit une valeur qui indique si les valeurs nulles sont autorisées dans cette colonne pour les lignes qui appartiennent à la table. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Définit une valeur qui indique si la colonne incrémente automatiquement la valeur de la colonne pour les nouvelles lignes ajoutées à la table. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Définit la valeur de départ d'une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Définit l'incrément utilisé par une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true. |
| [setCaption(String value)](#setCaption-java.lang.String) | Définit la légende de la colonne. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Définit le [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la colonne. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Définit le nom de la colonne dans le [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Définit le type de données stockées dans la colonne. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Définit la valeur par défaut de la colonne lors de la création de nouvelles lignes. |
| [setMaxLength(int value)](#setMaxLength-int) | Définit la longueur maximale d'une colonne de texte. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Définit l'espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Modifie l'ordre ou la position du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à l'ordre ou à la position spécifiés. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Définit un préfixe XML qui alias l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Définit une valeur indiquant si la colonne autorise les modifications dès qu'une ligne a été ajoutée à la table. |
| [setUnique(boolean value)](#setUnique-boolean) | Définit une valeur indiquant si les valeurs de chaque ligne de la colonne doivent être uniques. |
| [toString()](#toString) | Obtient le [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) de la colonne, s'il existe. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Initialise une nouvelle instance d'une classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de type chaîne.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) de type chaîne, en utilisant le nom de colonne spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Une chaîne qui représente le nom de la colonne à créer. Si elle est définie sur null ou une chaîne vide (""), un nom par défaut sera spécifié lors de l'ajout à la collection de colonnes. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Initialise une nouvelle instance de la classe @\{link DataColumn\} en utilisant le nom de colonne spécifié et la table à laquelle elle appartient.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | nom du DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la table à laquelle cette colonne appartient |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) en utilisant le nom de colonne spécifié et le type de données.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | Une chaîne qui représente le nom de la colonne à créer. Si elle est définie sur null ou une chaîne vide (""), un nom par défaut sera spécifié lors de l'ajout à la collection de colonnes. |
| dataType | java.lang.Class | Un [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) pris en charge. |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Initialise une nouvelle instance de la classe [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) en utilisant le nom de colonne spécifié, le type de données et le tableau de données auquel elle appartient.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | nom du DataColumn |
| type | java.lang.Class | type de données |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | la table à laquelle cette colonne appartient |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Obtient une valeur qui indique si les valeurs null sont autorisées dans cette colonne pour les lignes appartenant au tableau.

**Returns:**
booléen - true si les valeurs null sont autorisées ; sinon, false. La valeur par défaut est true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Obtient une valeur qui indique si la colonne incrémente automatiquement la valeur de la colonne pour les nouvelles lignes ajoutées à la table.

**Returns:**
booléen - true si la valeur de la colonne s'incrémente automatiquement ; sinon, false. La valeur par défaut est false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Obtient la valeur de départ d'une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true.

**Returns:**
long - La valeur de départ pour la fonctionnalité [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean).
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Obtient l'incrément utilisé par une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true.

**Returns:**
long - Le nombre par lequel la valeur de la colonne est automatiquement incrémentée. La valeur par défaut est 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Obtient la légende de la colonne.

**Returns:**
java.lang.String - La légende de la colonne. Si non définie, renvoie la valeur [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Obtient le [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la colonne.

**Returns:**
int - L'une des valeurs de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). La valeur renvoyée est l'une des constantes de [MappingType](../../com.aspose.words.net.system.data/mappingtype/).
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Obtient le nom de la colonne dans le [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String - Le nom de la colonne.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Obtient le type de données stockées dans la colonne.

**Returns:**
java.lang.Class - Un objet java.lang.Class qui représente le type de données de la colonne.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Obtient la valeur par défaut de la colonne lors de la création de nouvelles lignes.

**Returns:**
java.lang.Object - Une valeur appropriée au [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la colonne.
### getExpression() {#getExpression}
```
public String getExpression()
```


Obtient l'expression utilisée pour filtrer les lignes, calculer les valeurs d'une colonne ou créer une colonne agrégée.

**Returns:**
java.lang.String - Une expression pour calculer la valeur d'une colonne, ou créer une colonne agrégée. Le type de retour d'une expression est déterminé par le [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) de la colonne.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Obtient la longueur maximale d'une colonne texte.

**Returns:**
int - La longueur maximale de la colonne en caractères. Si la colonne n'a pas de longueur maximale, la valeur est -1 (par défaut).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtient l'espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String - L'espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Obtient la position de la colonne dans la collection [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
int - La position de la colonne. Renvoie -1 si la colonne n'est pas membre d'une collection.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Obtient un préfixe XML qui alias l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - Le préfixe XML pour l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Obtient une valeur qui indique si la colonne autorise les modifications dès qu'une ligne a été ajoutée à la table.

**Returns:**
booléen - true si la colonne est en lecture seule ; sinon, false. La valeur par défaut est false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Obtient le [DataTable](../../com.aspose.words.net.system.data/datatable/) auquel la colonne appartient.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Obtient une valeur qui indique si les valeurs de chaque ligne de la colonne doivent être uniques.

**Returns:**
booléen - true si la valeur doit être unique ; sinon, false. La valeur par défaut est false.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


Définit une valeur qui indique si les valeurs nulles sont autorisées dans cette colonne pour les lignes qui appartiennent à la table.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | true si les valeurs null sont autorisées ; sinon, false. La valeur par défaut est true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Définit une valeur qui indique si la colonne incrémente automatiquement la valeur de la colonne pour les nouvelles lignes ajoutées à la table.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | true si la valeur de la colonne s’incrémente automatiquement ; sinon, false. La valeur par défaut est false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Définit la valeur de départ d'une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | long | La valeur de départ pour la fonctionnalité [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Définit l'incrément utilisé par une colonne dont la propriété [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) est définie sur true.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | long | Le nombre par lequel la valeur de la colonne est automatiquement incrémentée. La valeur par défaut est 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Définit la légende de la colonne.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | La légende de la colonne. Si non définie, renvoie la valeur [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Définit le [MappingType](../../com.aspose.words.net.system.data/mappingtype/) de la colonne.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | L’une des valeurs de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). La valeur doit être l’une des constantes de [MappingType](../../com.aspose.words.net.system.data/mappingtype/). |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Définit le nom de la colonne dans le [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom de la colonne. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Définit le type de données stockées dans la colonne.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.Class | Un objet java.lang.Class qui représente le type de données de la colonne. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Définit la valeur par défaut de la colonne lors de la création de nouvelles lignes.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | Une valeur appropriée à la [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Définit la longueur maximale d'une colonne de texte.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La longueur maximale de la colonne en caractères. Si la colonne n’a pas de longueur maximale, la valeur est -1 (par défaut). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Définit l'espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | L’espace de noms du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Modifie l'ordre ou la position du [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) à l'ordre ou à la position spécifiés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| ordinal | int | L’ordinal spécifié. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Définit un préfixe XML qui alias l'espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Le préfixe XML pour l’espace de noms du [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Définit une valeur indiquant si la colonne autorise les modifications dès qu'une ligne a été ajoutée à la table.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | true si la colonne est en lecture seule ; sinon, false. La valeur par défaut est false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Définit une valeur indiquant si les valeurs de chaque ligne de la colonne doivent être uniques.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | true si la valeur doit être unique ; sinon, false. La valeur par défaut est false. |

### toString() {#toString}
```
public String toString()
```


Obtient le [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) de la colonne, s'il existe.

**Returns:**
java.lang.String - La valeur [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) si la propriété est définie ; sinon, la propriété [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
