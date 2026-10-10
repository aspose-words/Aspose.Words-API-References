---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words für Java"
description: "Stellt das Schema einer Spalte in einer DataTable in Java dar."
type: docs
weight: 14
url: /de/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Stellt das Schema einer Spalte in einer [DataTable](../../com.aspose.words.net.system.data/datatable/) dar.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataColumn()](#DataColumn) | Initialisiert eine neue Instanz einer [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse vom Typ string. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse vom Typ string unter Verwendung des angegebenen Spaltennamens. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Initialisiert eine neue Instanz der @\{link DataColumn\} Klasse mit dem angegebenen Spaltennamen und der Tabelle, zu der sie gehört. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse mit dem angegebenen Spaltennamen und Datentyp. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse mit dem angegebenen Spaltennamen, Datentyp und der Datentabelle, zu der sie gehört. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Gibt einen Wert zurück, der angibt, ob Nullwerte in dieser Spalte für Zeilen, die zur Tabelle gehören, erlaubt sind. |
| [getAutoIncrement()](#getAutoIncrement) | Gibt einen Wert zurück, der angibt, ob die Spalte den Wert für neue Zeilen, die zur Tabelle hinzugefügt werden, automatisch inkrementiert. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Gibt den Startwert für eine Spalte zurück, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Gibt das Inkrement zurück, das von einer Spalte verwendet wird, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist. |
| [getCaption()](#getCaption) | Gibt die Beschriftung der Spalte zurück. |
| [getColumnMapping()](#getColumnMapping) | Gibt den [MappingType](../../com.aspose.words.net.system.data/mappingtype/) der Spalte zurück. |
| [getColumnName()](#getColumnName) | Gibt den Namen der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) zurück. |
| [getDataType()](#getDataType) | Gibt den Typ der in der Spalte gespeicherten Daten zurück. |
| [getDefaultValue()](#getDefaultValue) | Gibt den Standardwert der Spalte zurück, wenn neue Zeilen erstellt werden. |
| [getExpression()](#getExpression) | Gibt den Ausdruck zurück, der zum Filtern von Zeilen, Berechnen von Werten in einer Spalte oder Erstellen einer Aggregatspalte verwendet wird. |
| [getMaxLength()](#getMaxLength) | Gibt die maximale Länge einer Textspalte zurück. |
| [getNamespace()](#getNamespace) | Gibt den Namespace der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) zurück. |
| [getOrdinal()](#getOrdinal) | Gibt die Position der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) Sammlung zurück. |
| [getPrefix()](#getPrefix) | Gibt ein XML-Präfix zurück, das den Namespace der [DataTable](../../com.aspose.words.net.system.data/datatable/) aliasiert. |
| [getReadOnly()](#getReadOnly) | Gibt einen Wert zurück, der angibt, ob die Spalte Änderungen zulässt, sobald eine Zeile zur Tabelle hinzugefügt wurde. |
| [getTable()](#getTable) | Gibt die [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, zu der die Spalte gehört. |
| [getUnique()](#getUnique) | Gibt einen Wert zurück, der angibt, ob die Werte in jeder Zeile der Spalte eindeutig sein müssen. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Legt einen Wert fest, der angibt, ob Nullwerte in dieser Spalte für Zeilen, die zur Tabelle gehören, erlaubt sind. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Legt einen Wert fest, der angibt, ob die Spalte den Wert für neue Zeilen, die zur Tabelle hinzugefügt werden, automatisch inkrementiert. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Legt den Startwert für eine Spalte fest, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Legt den von einer Spalte verwendeten Inkrement fest, wenn die Eigenschaft [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) auf true gesetzt ist. |
| [setCaption(String value)](#setCaption-java.lang.String) | Legt die Beschriftung für die Spalte fest. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Legt den [MappingType](../../com.aspose.words.net.system.data/mappingtype/) der Spalte fest. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Legt den Namen der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) fest. |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Legt den Typ der in der Spalte gespeicherten Daten fest. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Legt den Standardwert für die Spalte fest, wenn neue Zeilen erstellt werden. |
| [setMaxLength(int value)](#setMaxLength-int) | Legt die maximale Länge einer Textspalte fest. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Legt den Namespace des [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) fest. |
| [setOrdinal(int ordinal)](#setOrdinal-int) | Ändert die Ordnungszahl oder Position des [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) auf die angegebene Ordnungszahl oder Position. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | Legt ein XML-Präfix fest, das den Namespace der [DataTable](../../com.aspose.words.net.system.data/datatable/) aliasiert. |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Legt einen Wert fest, der angibt, ob die Spalte Änderungen zulässt, sobald eine Zeile zur Tabelle hinzugefügt wurde. |
| [setUnique(boolean value)](#setUnique-boolean) | Legt einen Wert fest, der angibt, ob die Werte in jeder Zeile der Spalte eindeutig sein müssen. |
| [toString()](#toString) | Ruft die [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) der Spalte ab, falls vorhanden. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Initialisiert eine neue Instanz einer [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse vom Typ string.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse vom Typ string unter Verwendung des angegebenen Spaltennamens.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Eine Zeichenkette, die den Namen der zu erstellenden Spalte darstellt. Wird sie auf null oder eine leere Zeichenkette (\"\"), gesetzt, wird beim Hinzufügen zur Spaltensammlung ein Standardname festgelegt. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Initialisiert eine neue Instanz der @\{link DataColumn\} Klasse mit dem angegebenen Spaltennamen und der Tabelle, zu der sie gehört.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Name des DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | die Tabelle, zu der diese Spalte gehört |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse mit dem angegebenen Spaltennamen und Datentyp.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Eine Zeichenkette, die den Namen der zu erstellenden Spalte darstellt. Wird sie auf null oder eine leere Zeichenkette (\"\"), gesetzt, wird beim Hinzufügen zur Spaltensammlung ein Standardname festgelegt. |
| dataType | java.lang.Class | Ein unterstütztes [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Initialisiert eine neue Instanz der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Klasse mit dem angegebenen Spaltennamen, Datentyp und der Datentabelle, zu der sie gehört.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Name des DataColumn |
| Typ | java.lang.Class | Datentyp |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | die Tabelle, zu der diese Spalte gehört |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Gibt einen Wert zurück, der angibt, ob Nullwerte in dieser Spalte für Zeilen, die zur Tabelle gehören, erlaubt sind.

**Returns:**
boolean - true, wenn Nullwerte erlaubt sind; andernfalls false. Der Standardwert ist true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Gibt einen Wert zurück, der angibt, ob die Spalte den Wert für neue Zeilen, die zur Tabelle hinzugefügt werden, automatisch inkrementiert.

**Returns:**
boolean - true, wenn der Wert der Spalte automatisch inkrementiert wird; andernfalls false. Der Standardwert ist false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Gibt den Startwert für eine Spalte zurück, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist.

**Returns:**
long - Der Startwert für die [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean)-Funktion.
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Gibt das Inkrement zurück, das von einer Spalte verwendet wird, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist.

**Returns:**
long - Die Zahl, um die der Wert der Spalte automatisch inkrementiert wird. Der Standardwert ist 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Gibt die Beschriftung der Spalte zurück.

**Returns:**
java.lang.String - Die Beschriftung der Spalte. Wenn nicht gesetzt, wird der Wert von [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) zurückgegeben.
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Gibt den [MappingType](../../com.aspose.words.net.system.data/mappingtype/) der Spalte zurück.

**Returns:**
int - Einer der [MappingType](../../com.aspose.words.net.system.data/mappingtype/)-Werte. Der zurückgegebene Wert ist einer der [MappingType](../../com.aspose.words.net.system.data/mappingtype/)-Konstanten.
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Gibt den Namen der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) zurück.

**Returns:**
java.lang.String - Der Name der Spalte.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Gibt den Typ der in der Spalte gespeicherten Daten zurück.

**Returns:**
java.lang.Class - Ein java.lang.Class-Objekt, das den Datentyp der Spalte darstellt.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Gibt den Standardwert der Spalte zurück, wenn neue Zeilen erstellt werden.

**Returns:**
java.lang.Object - Ein Wert, der zum Spaltentyp passt, [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class).
### getExpression() {#getExpression}
```
public String getExpression()
```


Gibt den Ausdruck zurück, der zum Filtern von Zeilen, Berechnen von Werten in einer Spalte oder Erstellen einer Aggregatspalte verwendet wird.

**Returns:**
java.lang.String - Ein Ausdruck, um den Wert einer Spalte zu berechnen oder eine Aggregatspalte zu erstellen. Der Rückgabetyp eines Ausdrucks wird durch den [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) der Spalte bestimmt.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Gibt die maximale Länge einer Textspalte zurück.

**Returns:**
int - Die maximale Länge der Spalte in Zeichen. Hat die Spalte keine maximale Länge, ist der Wert -1 (Standard).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Gibt den Namespace der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) zurück.

**Returns:**
java.lang.String - Der Namensraum der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Gibt die Position der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) Sammlung zurück.

**Returns:**
int - Die Position der Spalte. Gibt -1 zurück, wenn die Spalte kein Mitglied einer Sammlung ist.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


Gibt ein XML-Präfix zurück, das den Namespace der [DataTable](../../com.aspose.words.net.system.data/datatable/) aliasiert.

**Returns:**
java.lang.String - Das XML-Präfix für den Namensraum der [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Gibt einen Wert zurück, der angibt, ob die Spalte Änderungen zulässt, sobald eine Zeile zur Tabelle hinzugefügt wurde.

**Returns:**
boolean - true, wenn die Spalte schreibgeschützt ist; andernfalls false. Der Standardwert ist false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gibt die [DataTable](../../com.aspose.words.net.system.data/datatable/) zurück, zu der die Spalte gehört.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Gibt einen Wert zurück, der angibt, ob die Werte in jeder Zeile der Spalte eindeutig sein müssen.

**Returns:**
boolean - true, wenn der Wert eindeutig sein muss; andernfalls false. Der Standardwert ist false.
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


Legt einen Wert fest, der angibt, ob Nullwerte in dieser Spalte für Zeilen, die zur Tabelle gehören, erlaubt sind.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | true, wenn Nullwerte erlaubt sind; andernfalls false. Der Standardwert ist true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Legt einen Wert fest, der angibt, ob die Spalte den Wert für neue Zeilen, die zur Tabelle hinzugefügt werden, automatisch inkrementiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | true, wenn der Wert der Spalte automatisch inkrementiert wird; andernfalls false. Der Standardwert ist false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Legt den Startwert für eine Spalte fest, deren [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) Eigenschaft auf true gesetzt ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | long | Der Startwert für die Funktion [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Legt den von einer Spalte verwendeten Inkrement fest, wenn die Eigenschaft [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) auf true gesetzt ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | long | Die Zahl, um die der Wert der Spalte automatisch inkrementiert wird. Der Standardwert ist 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Legt die Beschriftung für die Spalte fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Die Beschriftung der Spalte. Wenn nicht gesetzt, wird der Wert von [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) zurückgegeben. |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Legt den [MappingType](../../com.aspose.words.net.system.data/mappingtype/) der Spalte fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Einer der Werte von [MappingType](../../com.aspose.words.net.system.data/mappingtype/). Der Wert muss einer der Konstanten von [MappingType](../../com.aspose.words.net.system.data/mappingtype/) sein. |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Legt den Namen der Spalte in der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name der Spalte. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Legt den Typ der in der Spalte gespeicherten Daten fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.Class | Ein java.lang.Class-Objekt, das den Datentyp der Spalte darstellt. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Legt den Standardwert für die Spalte fest, wenn neue Zeilen erstellt werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.Object | Ein Wert, der zum Datentyp der Spalte passt, [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Legt die maximale Länge einer Textspalte fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die maximale Länge der Spalte in Zeichen. Hat die Spalte keine maximale Länge, ist der Wert -1 (Standard). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Legt den Namespace des [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Namensraum der [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


Ändert die Ordnungszahl oder Position des [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) auf die angegebene Ordnungszahl oder Position.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ordinal | int | Der angegebene Ordnungswert. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


Legt ein XML-Präfix fest, das den Namespace der [DataTable](../../com.aspose.words.net.system.data/datatable/) aliasiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Das XML-Präfix für den Namensraum der [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Legt einen Wert fest, der angibt, ob die Spalte Änderungen zulässt, sobald eine Zeile zur Tabelle hinzugefügt wurde.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | true, wenn die Spalte schreibgeschützt ist; andernfalls false. Der Standardwert ist false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Legt einen Wert fest, der angibt, ob die Werte in jeder Zeile der Spalte eindeutig sein müssen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | true, wenn der Wert eindeutig sein muss; andernfalls false. Der Standardwert ist false. |

### toString() {#toString}
```
public String toString()
```


Ruft die [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) der Spalte ab, falls vorhanden.

**Returns:**
java.lang.String - Der [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) Wert, wenn die Eigenschaft gesetzt ist; andernfalls die [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) Eigenschaft.
