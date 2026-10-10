---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words für Java"
description: "Stellt Informationen über einen einzelnen Datensatz in einer externen Datenquelle dar, der vom Seriendruck in Java ausgeschlossen werden soll."
type: docs
weight: 492
url: /de/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Stellt Informationen über einen einzelnen Datensatz in einer externen Datenquelle dar, der vom Seriendruck ausgeschlossen werden soll.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Wenn ein Datensatz in ein zusammengeführtes Dokument eingefügt werden soll, werden keine Informationen zu diesem Datensatz benötigt. Wenn jedoch ein bestimmter Datensatz nicht in ein zusammengeführtes Dokument eingefügt werden soll, muss der Wert des eindeutigen Schlüssels für diesen Datensatz in der [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte)-Eigenschaft dieses Objekts gespeichert werden, um diesen Ausschluss anzuzeigen.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [getActive()](#getActive) | Gibt an, ob der Datensatz aus der Datenquelle in ein Dokument importiert werden soll, wenn der Seriendruck ausgeführt wird. |
| [getColumn()](#getColumn) | Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. |
| [getHash()](#getHash) | Stellt den Hashcode für diesen Datensatz dar. |
| [getUniqueTag()](#getUniqueTag) | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. |
| [setActive(boolean value)](#setActive-boolean) | Gibt an, ob der Datensatz aus der Datenquelle in ein Dokument importiert werden soll, wenn der Seriendruck ausgeführt wird. |
| [setColumn(int value)](#setColumn-int) | Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. |
| [setHash(int value)](#setHash-int) | Stellt den Hashcode für diesen Datensatz dar. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Gibt eine tiefe Kopie dieses Objekts zurück.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Gibt an, ob der Datensatz aus der Datenquelle in ein Dokument importiert werden soll, wenn der Seriendruck ausgeführt wird. Der Standardwert ist true.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getColumn() {#getColumn}
```
public int getColumn()
```


Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0.

**Returns:**
int - Der entsprechende int-Wert.
### getHash() {#getHash}
```
public int getHash()
```


Stellt den Hashcode für diesen Datensatz dar. Manchmal verwendet Microsoft Word [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) eines gesamten Datensatzes anstelle eines [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte)-Werts. Der Standardwert ist 0.

**Returns:**
int - Der entsprechende int-Wert.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. Der Standardwert ist null.

**Returns:**
byte[] - Der entsprechende byte[]-Wert.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Gibt an, ob der Datensatz aus der Datenquelle in ein Dokument importiert werden soll, wenn der Seriendruck ausgeführt wird. Der Standardwert ist true.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Stellt den Hashcode für diesen Datensatz dar. Manchmal verwendet Microsoft Word [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) eines gesamten Datensatzes anstelle eines [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte)-Werts. Der Standardwert ist 0.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. Der Standardwert ist null.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | byte[] | Der entsprechende byte[]-Wert. |

