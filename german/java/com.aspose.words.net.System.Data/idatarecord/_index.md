---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words für Java"
description: "Bietet Zugriff auf die Spaltenwerte jeder Zeile für einen DataReader und wird von .NET Framework-Datenanbietern implementiert, die relationale Datenbanken in Java zugreifen."
type: docs
weight: 35
url: /de/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Stellt Zugriff auf die Spaltenwerte jeder Zeile für einen DataReader bereit und wird von .NET Framework-Datenanbietern implementiert, die relationale Datenbanken zugreifen.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int i)](#get-int) | Ruft die Spalte ab, die sich am angegebenen Index befindet. |
| [getFieldCount()](#getFieldCount) | Ruft die Anzahl der Spalten in der aktuellen Zeile ab. |
| [getFieldType(int i)](#getFieldType-int) | Ruft die java.lang.Class-Information ab, die dem Typ von java.lang.Object entspricht, der von [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) zurückgegeben würde. |
| [getName(int i)](#getName-int) | Ruft den Namen des zu findenden Feldes ab. |
| [getValue(int i)](#getValue-int) | Gibt den Wert des angegebenen Feldes zurück. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Ruft die Spalte ab, die sich am angegebenen Index befindet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| i | int | Der nullbasierte Index der abzurufenden Spalte. |

**Returns:**
java.lang.Object – Die Spalte, die sich am angegebenen Index befindet, als java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Ruft die Anzahl der Spalten in der aktuellen Zeile ab.

**Returns:**
int – Wenn nicht in einem gültigen Recordset positioniert, 0; andernfalls die Anzahl der Spalten im aktuellen Datensatz. Der Standardwert ist -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Ruft die java.lang.Class-Information ab, die dem Typ von java.lang.Object entspricht, der von [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) zurückgegeben würde.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| i | int | Der Index des zu findenden Feldes. |

**Returns:**
java.lang.Class – Die java.lang.Class-Information, die dem Typ von java.lang.Object entspricht, der von [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) zurückgegeben würde.
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Ruft den Namen des zu findenden Feldes ab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| i | int | Der Index des zu findenden Feldes. |

**Returns:**
java.lang.String – Der Name des Feldes oder die leere Zeichenkette (""), falls kein Wert zurückgegeben werden kann.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Gibt den Wert des angegebenen Feldes zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| i | int | Der Index des zu findenden Feldes. |

**Returns:**
java.lang.Object – Das java.lang.Object, das den Feldwert bei Rückgabe enthält.
