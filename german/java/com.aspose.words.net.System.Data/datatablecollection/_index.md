---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words für Java"
description: "Stellt die Sammlung von Tabellen für das DataSet in Java dar."
type: docs
weight: 26
url: /de/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

Stellt die Sammlung von Tabellen für das [DataSet](../../com.aspose.words.net.system.data/dataset/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Fügt die angegebene DataTable zur Sammlung hinzu. |
| [add(String name)](#add-java.lang.String) | Erstellt ein [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen und fügt es zur Sammlung hinzu. |
| [contains(String name)](#contains-java.lang.String) | Gibt einen Wert zurück, der angibt, ob ein [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen in der Sammlung existiert. |
| [get(int index)](#get-int) | Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt am angegebenen Index zurück. |
| [get(String name)](#get-java.lang.String) | Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen zurück. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen im angegebenen Namensraum zurück. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Entfernt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen aus der Sammlung. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Fügt die angegebene DataTable zur Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Das hinzuzufügende DataTable-Objekt. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Erstellt ein [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen und fügt es zur Sammlung hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name, der dem erstellten [DataTable](../../com.aspose.words.net.system.data/datatable/) zugewiesen wird. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Gibt einen Wert zurück, der angibt, ob ein [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen in der Sammlung existiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des zu findenden [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
boolescher Wert – true, wenn die angegebene Tabelle existiert; andernfalls false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt am angegebenen Index zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int | Der nullbasierte Index des zu findenden [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des zu findenden DataTable. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Gibt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen im angegebenen Namensraum zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des zu findenden DataTable. |
| tableNamespace | java.lang.String | Der Name des [DataTable](../../com.aspose.words.net.system.data/datatable/)-Namensraums, in dem gesucht werden soll. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int – Gesamtzahl der Elemente in dieser Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Entfernt das [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekt mit dem angegebenen Namen aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String | Der Name des zu entfernenden [DataTable](../../com.aspose.words.net.system.data/datatable/)-Objekts. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
