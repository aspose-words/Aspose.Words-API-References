---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Zeilen für eine DataTable in Java dar."
type: docs
weight: 21
url: /de/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Stellt eine Sammlung von Zeilen für eine [DataTable](../../com.aspose.words.net.system.data/datatable/) dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Fügt das angegebene [DataRow](../../com.aspose.words.net.system.data/datarow/) dem Objekt [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) hinzu. |
| [add(Object[] values)](#add-java.lang.Object...) | Erstellt eine Zeile mit den angegebenen Werten und fügt sie der [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) hinzu. |
| [clear()](#clear) | Leert die Sammlung aller Zeilen. |
| [find(Object[] keys)](#find-java.lang.Object) | Gibt die Zeile zurück, die die angegebenen Primärschlüsselwerte enthält. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Gibt die durch den Primärschlüsselwert angegebene Zeile zurück. |
| [get(int index)](#get-int) | Gibt die Zeile am angegebenen Index zurück. |
| [get(Object[] values)](#get-java.lang.Object) | Gibt die Zeile zurück, die die angegebenen Werte enthält. |
| [getCount()](#getCount) | Gibt die Gesamtzahl der [DataRow](../../com.aspose.words.net.system.data/datarow/)‑Objekte in dieser Sammlung zurück. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Fügt an der angegebenen Position eine neue Zeile in die Sammlung ein. |
| [iterator()](#iterator) | Gibt einen java.util.Iterator für diese Sammlung zurück. |
| [removeAt(int index)](#removeAt-int) | Entfernt die Zeile am angegebenen Index aus der Sammlung. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Fügt das angegebene [DataRow](../../com.aspose.words.net.system.data/datarow/) dem Objekt [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Das hinzuzufügende [DataRow](../../com.aspose.words.net.system.data/datarow/). |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Erstellt eine Zeile mit den angegebenen Werten und fügt sie der [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Werte | java.lang.Object[] | Das Array von Werten, das zum Erstellen der neuen Zeile verwendet wird. |

### clear() {#clear}
```
public void clear()
```


Leert die Sammlung aller Zeilen.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Gibt die Zeile zurück, die die angegebenen Primärschlüsselwerte enthält.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Schlüssel | java.lang.Object[] | Ein Array von Primärschlüsselwerten zum Suchen. Der Typ des Arrays ist Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Gibt die durch den Primärschlüsselwert angegebene Zeile zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | Der Primärschlüsselwert des zu findenden DataRow. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Gibt die Zeile am angegebenen Index zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der nullbasierte Index der zurückzugebenden Zeile. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Gibt die Zeile zurück, die die angegebenen Werte enthält. Wenn Spalten des Primärschlüssels vorhanden sind, wird der Index verwendet. Wenn kein Index vorhanden ist, wird ein einfacher linearer Scan verwendet. Seien Sie dabei vorsichtig, da dies erheblich viel Zeit in Anspruch nehmen kann.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Werte | java.lang.Object[] | Daten der Zeile |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Gesamtzahl der [DataRow](../../com.aspose.words.net.system.data/datarow/)‑Objekte in dieser Sammlung zurück.

**Returns:**
int - Die Gesamtzahl der [DataRow](../../com.aspose.words.net.system.data/datarow/) Objekte in dieser Sammlung.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Fügt an der angegebenen Position eine neue Zeile in die Sammlung ein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Das hinzuzufügende [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| Pos | int | Der (nullbasierte) Ort in der Sammlung, an dem Sie die DataRow hinzufügen möchten. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt einen java.util.Iterator für diese Sammlung zurück.

**Returns:**
java.util.Iterator - Ein java.util.Iterator für diese Sammlung.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt die Zeile am angegebenen Index aus der Sammlung.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Der Index der zu entfernenden Zeile. |

