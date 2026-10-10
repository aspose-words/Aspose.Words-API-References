---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words für Java"
description: "Stellt die Sammlung von DataRelation-Objekten für dieses DataSet in Java dar."
type: docs
weight: 19
url: /de/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Stellt die Sammlung von [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekten für dieses [DataSet](../../com.aspose.words.net.system.data/dataset/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit einer angegebenen Eltern- und Kindspalte und fügt sie der Sammlung hinzu. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Fügt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) zur [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) hinzu. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Fügt der Sammlung eine Relation hinzu. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Fügt der Sammlung eine Relation hinzu. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen sowie Eltern- und Kindspalten und fügt sie der Sammlung hinzu. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, Eltern- und Kindspalten, mit optionalen Einschränkungen gemäß dem Wert des Parameters  createConstraints , und fügt sie der Sammlung hinzu. |
| [clear()](#clear) | Leert die Sammlung von allen Relationen. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Überprüft, ob eine DataRelation mit dem angegebenen Namen (Groß-/Kleinschreibung ignorierend) in der Sammlung existiert. |
| [get(int index)](#get-int) | Liefert das [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekt am angegebenen Index. |
| [get(String name)](#get-java.lang.String) | Liefert das [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekt, das durch den Namen angegeben ist. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Liefert den Index des angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekts. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Entfernt die Relation am angegebenen Index aus der Sammlung. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit einer angegebenen Eltern- und Kindspalte und fügt sie der Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Elternspalte der Relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Kindspalte der Relation. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Fügt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) zur [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Die DataRelation, die zur Sammlung hinzugefügt werden soll. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Fügt der Sammlung eine Relation hinzu. Führt keine Prüfungen auf Duplikate usw. durch.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die Eltertabelle der Relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die untergeordnete Tabelle der Relation. |
| parentColumnName | java.lang.String | Der Name der übergeordneten Spalte der Relation. |
| childColumnName | java.lang.String | Der Name der untergeordneten Spalte der Relation. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Fügt der Sammlung eine Relation hinzu. Führt keine Prüfungen auf Duplikate usw. durch.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die Eltertabelle der Relation. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Die untergeordnete Tabelle der Relation. |
| parentColumnNames | java.lang.String[] | Das Array der Namen der übergeordneten Spalten der Relation. |
| childColumnNames | java.lang.String[] | Das Array der Namen der untergeordneten Spalten der Relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen sowie Eltern- und Kindspalten und fügt sie der Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Elternspalte der Relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Kindspalte der Relation. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Erstellt eine [DataRelation](../../com.aspose.words.net.system.data/datarelation/) mit dem angegebenen Namen, Eltern- und Kindspalten, mit optionalen Einschränkungen gemäß dem Wert des Parameters  createConstraints , und fügt sie der Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Relation. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Elternspalte der Relation. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die Kindspalte der Relation. |
| createConstraints | boolean | true, um Einschränkungen zu erstellen; andernfalls false. (Standard ist true). |

### clear() {#clear}
```
public void clear()
```


Leert die Sammlung von allen Relationen.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Überprüft, ob eine DataRelation mit dem angegebenen Namen (Groß-/Kleinschreibung ignorierend) in der Sammlung existiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Der Name der zu findenden Relation. |

**Returns:**
boolean – true, wenn eine Relation mit dem angegebenen Namen existiert; andernfalls false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Liefert das [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekt am angegebenen Index.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index zum Suchen. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


Liefert das [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekt, das durch den Namen angegeben ist.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der zu findenden Relation. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int – die Gesamtzahl der Elemente in einer Sammlung
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Liefert den Index des angegebenen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) Objekts.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Die zu suchende Relation. |

**Returns:**
int – Der nullbasierte Index der Relation oder -1, wenn die Relation nicht in der Sammlung gefunden wird.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt die Relation am angegebenen Index aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der Index der zu entfernenden Relation. |

