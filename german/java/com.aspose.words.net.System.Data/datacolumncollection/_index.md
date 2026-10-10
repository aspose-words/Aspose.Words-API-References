---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von DataColumn-Objekten für ein DataTable in Java dar."
type: docs
weight: 15
url: /de/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Stellt eine Sammlung von [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekten für ein [DataTable](../../com.aspose.words.net.system.data/datatable/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Erstellt das angegebene [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu. |
| [add(String columnName)](#add-java.lang.String) | Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt mit dem angegebenen Namen und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu. |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt mit dem angegebenen Namen und Typ und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu. |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) mit dem angegebenen Namen, Typ und spezifischen Werten und fügt es der Spaltensammlung hinzu. |
| [clear()](#clear) | Leert die Sammlung von allen Spalten. |
| [contains(String name)](#contains-java.lang.String) | Prüft, ob die Sammlung eine Spalte mit dem angegebenen Namen enthält. |
| [get(int index)](#get-int) | Gibt das [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) aus der Sammlung am angegebenen Index zurück. |
| [get(String name)](#get-java.lang.String) | Ruft die [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) aus der Sammlung mit dem angegebenen Namen ab. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Ruft den Index einer nach Namen angegebenen Spalte ab. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Ruft den Index der Spalte mit dem angegebenen Namen ab (der Name ist nicht groß-/kleinschreibungssensitiv). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Entfernt das angegebene [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekt aus der Sammlung. |
| [remove(String name)](#remove-java.lang.String) | Entfernt das [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekt, das den angegebenen Namen hat, aus der Sammlung. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Erstellt das angegebene [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Das hinzuzufügende [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt mit dem angegebenen Namen und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Der Name der Spalte. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)-Objekt mit dem angegebenen Namen und Typ und fügt es der [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Der [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) zu verwenden, wenn Sie die Spalte erstellen. |
| type | java.lang.Class | Der [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) der neuen Spalte. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Erstellt ein [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) mit dem angegebenen Namen, Typ und spezifischen Werten und fügt es der Spaltensammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | name |
| Typ | java.lang.Class | Datentyp |
| columnMapping | int | Spaltenzuordnungstyp |
| allowAutoIncrement | boolean | Ist Auto‑Inkrement erlaubt |
| allowDBNull | boolean | Ist DBNull‑Wert erlaubt |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Leert die Sammlung von allen Spalten.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Prüft, ob die Sammlung eine Spalte mit dem angegebenen Namen enthält.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) der zu suchenden Spalte. |

**Returns:**
boolean - true, wenn eine Spalte mit diesem Namen existiert; andernfalls false.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Gibt das [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) aus der Sammlung am angegebenen Index zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index der zurückzugebenden Spalte. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Ruft die [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) aus der Sammlung mit dem angegebenen Namen ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) der zurückzugebenden Spalte. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - die Gesamtzahl der Elemente in einer Sammlung.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Ruft den Index einer nach Namen angegebenen Spalte ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Der Name der zurückzugebenden Spalte. |

**Returns:**
int - Der Index der durch  column  angegebenen Spalte, falls gefunden; andernfalls -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Ruft den Index der Spalte mit dem angegebenen Namen ab (der Name ist nicht groß-/kleinschreibungssensitiv).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| columnName | java.lang.String | Der Name der zu findenden Spalte. |

**Returns:**
int - Der nullbasierte Index der Spalte mit dem angegebenen Namen, oder -1, falls die Spalte nicht in der Sammlung existiert.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Entfernt das angegebene [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekt aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Die [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) zum Entfernen. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Entfernt das [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) Objekt, das den angegebenen Namen hat, aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name der Spalte zum Entfernen. |

