---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words für Java"
description: "Stellt einen In‑Memory‑Cache von Daten in Java dar."
type: docs
weight: 24
url: /de/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Stellt einen In‑Memory‑Cache von Daten dar.
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DataSet()](#DataSet) | Initialisiert eine neue Instanz der [DataSet](../../com.aspose.words.net.system.data/dataset/) Klasse. |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Initialisiert eine neue Instanz der DataSet‑Klasse mit Daten, die aus einer Connection übernommen wurden. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Initialisiert eine neue Instanz der DataSet‑Klasse mit Daten, die aus einer Connection übernommen wurden. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Initialisiert eine neue Instanz einer [DataSet](../../com.aspose.words.net.system.data/dataset/) Klasse mit dem angegebenen Namen. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Leert das [DataSet](../../com.aspose.words.net.system.data/dataset/) von allen Daten, indem alle Zeilen in allen Tabellen entfernt werden. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Gibt den Namen des aktuellen [DataSet](../../com.aspose.words.net.system.data/dataset/) zurück. |
| [getEnforceConstraints()](#getEnforceConstraints) | Gibt einen Wert zurück, der angibt, ob Einschränkungsregeln bei einem Update‑Vorgang befolgt werden. |
| [getNamespace()](#getNamespace) | Gibt den Namensraum des [DataSet](../../com.aspose.words.net.system.data/dataset/) zurück. |
| [getRelations()](#getRelations) | Ruft die Sammlung von Relationen ab, die Tabellen verknüpfen und die Navigation von übergeordneten Tabellen zu untergeordneten Tabellen ermöglichen. |
| [getTables()](#getTables) | Gibt die Sammlung von Tabellen zurück, die im [DataSet](../../com.aspose.words.net.system.data/dataset/) enthalten sind. |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Liest das XML‑Schema und die Daten in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein, wobei den angegebenen java.io.InputStream verwendet. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Liest das XML‑Schema und die Daten in das DataSet ein, wobei den angegebenen java.io.InputStream und [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) verwendet. |
| [readXml(String fileName)](#readXml-java.lang.String) | Liest das XML‑Schema und die Daten in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein, wobei die angegebene Datei verwendet wird. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Liest das XML‑Schema und die Daten in das DataSet ein, wobei die angegebene Datei und [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) verwendet werden. |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Liest das XML‑Schema aus dem angegebenen java.io.InputStream in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein. |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Liest das XML‑Schema aus der angegebenen Datei in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein. |
| [reset()](#reset) | Setzt das [DataSet](../../com.aspose.words.net.system.data/dataset/) auf den ursprünglichen Zustand zurück. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Setzt den Namen des aktuellen [DataSet](../../com.aspose.words.net.system.data/dataset/) fest. |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Setzt einen Wert, der angibt, ob Einschränkungsregeln bei einem Update‑Vorgang befolgt werden. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Setzt die Locale‑Informationen, die zum Vergleichen von Strings innerhalb der Tabelle verwendet werden. |
### DataSet() {#DataSet}
```
public DataSet()
```


Initialisiert eine neue Instanz der [DataSet](../../com.aspose.words.net.system.data/dataset/) Klasse.

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Initialisiert eine neue Instanz der DataSet‑Klasse mit Daten, die aus einer Connection übernommen wurden. Tabellen, Relationen, Einschränkungen und Indizes werden in das DataSet kopiert.

Standardmäßig wird kein Schemaname verwendet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Verbindung | java.sql.Connection | die DB-Daten enthält. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Initialisiert eine neue Instanz der DataSet‑Klasse mit Daten, die aus einer Connection übernommen wurden. Tabellen, Relationen, Einschränkungen und Indizes werden in das DataSet kopiert.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

oder

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Verbindung | java.sql.Connection | die DB-Daten enthält. |
| schemaName | java.lang.String | die zu importierenden Tabellen enthält. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Initialisiert eine neue Instanz einer [DataSet](../../com.aspose.words.net.system.data/dataset/) Klasse mit dem angegebenen Namen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSetName | java.lang.String | Der Name des [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean – true, wenn das Schema gelesen wurde
### clear() {#clear}
```
public void clear()
```


Leert das [DataSet](../../com.aspose.words.net.system.data/dataset/) von allen Daten, indem alle Zeilen in allen Tabellen entfernt werden.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Gibt den Namen des aktuellen [DataSet](../../com.aspose.words.net.system.data/dataset/) zurück.

**Returns:**
java.lang.String – Der Name des [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Gibt einen Wert zurück, der angibt, ob Einschränkungsregeln bei einem Update‑Vorgang befolgt werden.

**Returns:**
boolean – true, wenn Regeln durchgesetzt werden; andernfalls false. Der Standardwert ist true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Gibt den Namensraum des [DataSet](../../com.aspose.words.net.system.data/dataset/) zurück.

**Returns:**
java.lang.String – Der Namensraum des [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Ruft die Sammlung von Relationen ab, die Tabellen verknüpfen und die Navigation von übergeordneten Tabellen zu untergeordneten Tabellen ermöglichen.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Gibt die Sammlung von Tabellen zurück, die im [DataSet](../../com.aspose.words.net.system.data/dataset/) enthalten sind.

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean – true, wenn das Gebietsschema gesetzt wurde
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Liest das XML‑Schema und die Daten in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein, wobei den angegebenen java.io.InputStream verwendet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream | Ein Objekt, das von java.io.InputStream abgeleitet ist. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Liest das XML‑Schema und die Daten in das DataSet ein, wobei den angegebenen java.io.InputStream und [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) verwendet.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Der Stream, aus dem gelesen wird. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | Einer der Werte von [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Liest das XML‑Schema und die Daten in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein, wobei die angegebene Datei verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Dateiname (einschließlich Pfad), aus dem gelesen wird. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Liest das XML‑Schema und die Daten in das DataSet ein, wobei die angegebene Datei und [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xmlPath | java.lang.String | die angegebene Datei |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Liest das XML‑Schema aus dem angegebenen java.io.InputStream in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream | Der java.io.InputStream, aus dem gelesen wird. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Liest das XML‑Schema aus der angegebenen Datei in das [DataSet](../../com.aspose.words.net.system.data/dataset/) ein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Dateiname (einschließlich Pfad), aus dem gelesen wird. |

### reset() {#reset}
```
public void reset()
```


Setzt das [DataSet](../../com.aspose.words.net.system.data/dataset/) auf seinen ursprünglichen Zustand zurück. Unterklassen sollten [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) überschreiben, um ein [DataSet](../../com.aspose.words.net.system.data/dataset/) in seinen ursprünglichen Zustand zurückzuversetzen.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Setzt den Namen des aktuellen [DataSet](../../com.aspose.words.net.system.data/dataset/) fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | java.lang.String | Der Name des [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Setzt einen Wert, der angibt, ob Einschränkungsregeln bei einem Update‑Vorgang befolgt werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | true, wenn Regeln durchgesetzt werden; andernfalls false. Der Standardwert ist true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Setzt die Locale‑Informationen, die zum Vergleichen von Strings innerhalb der Tabelle verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| locale | java.util.Locale | dieses DataSet |

