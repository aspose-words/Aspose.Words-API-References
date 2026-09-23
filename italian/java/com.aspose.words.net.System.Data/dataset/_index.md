---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words per Java"
description: "Rappresenta una cache di dati in memoria in Java."
type: docs
weight: 24
url: /it/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Rappresenta una cache in memoria dei dati.
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [DataSet()](#DataSet) | Inizializza una nuova istanza della classe [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Inizializza una nuova istanza della classe DataSet con i dati prelevati da Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Inizializza una nuova istanza della classe DataSet con i dati prelevati da Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Inizializza una nuova istanza di una classe [DataSet](../../com.aspose.words.net.system.data/dataset/) con il nome fornito. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Cancella tutti i dati dal [DataSet](../../com.aspose.words.net.system.data/dataset/) rimuovendo tutte le righe in tutte le tabelle. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Ottiene il nome del corrente [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getEnforceConstraints()](#getEnforceConstraints) | Ottiene un valore che indica se le regole di vincolo sono rispettate durante qualsiasi operazione di aggiornamento. |
| [getNamespace()](#getNamespace) | Ottiene lo spazio dei nomi del [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | Ottieni la raccolta di relazioni che collegano le tabelle e consentono la navigazione dalle tabelle padre a quelle figlio. |
| [getTables()](#getTables) | Ottiene la raccolta di tabelle contenute nel [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Legge lo schema XML e i dati nel [DataSet](../../com.aspose.words.net.system.data/dataset/) utilizzando il java.io.InputStream specificato. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Legge lo schema XML e i dati nel DataSet utilizzando il java.io.InputStream specificato e [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | Legge lo schema XML e i dati nel [DataSet](../../com.aspose.words.net.system.data/dataset/) utilizzando il file specificato. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Legge lo schema XML e i dati nel DataSet utilizzando il file specificato e [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Legge lo schema XML dal java.io.InputStream specificato nel [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Legge lo schema XML dal file specificato nel [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | Ripristina il [DataSet](../../com.aspose.words.net.system.data/dataset/) al suo stato originale. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Imposta il nome del corrente [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Imposta un valore che indica se le regole di vincolo sono rispettate durante qualsiasi operazione di aggiornamento. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Imposta le informazioni locali utilizzate per confrontare le stringhe all'interno della tabella. |
### DataSet() {#DataSet}
```
public DataSet()
```


Inizializza una nuova istanza della classe [DataSet](../../com.aspose.words.net.system.data/dataset/).

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Inizializza una nuova istanza della classe DataSet con i dati prelevati da Connection. Tabelle, Relazioni, Vincoli e Indici saranno copiati nel DataSet.

Per impostazione predefinita non verrà utilizzato alcun nome di schema.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| connessione | java.sql.Connection | che contiene i dati del DB. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Inizializza una nuova istanza della classe DataSet con i dati prelevati da Connection. Tabelle, Relazioni, Vincoli e Indici saranno copiati nel DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

o

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| connessione | java.sql.Connection | che contiene i dati del DB. |
| schemaName | java.lang.String | che contiene le tabelle da importare. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Inizializza una nuova istanza di una classe [DataSet](../../com.aspose.words.net.system.data/dataset/) con il nome fornito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataSetName | java.lang.String | Il nome del [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - true se lo schema è stato letto
### clear() {#clear}
```
public void clear()
```


Cancella tutti i dati dal [DataSet](../../com.aspose.words.net.system.data/dataset/) rimuovendo tutte le righe in tutte le tabelle.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Ottiene il nome del corrente [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - Il nome del [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Ottiene un valore che indica se le regole di vincolo sono rispettate durante qualsiasi operazione di aggiornamento.

**Returns:**
boolean - true se le regole sono applicate; altrimenti false. Il valore predefinito è true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Ottiene lo spazio dei nomi del [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - Lo spazio dei nomi del [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Ottieni la raccolta di relazioni che collegano le tabelle e consentono la navigazione dalle tabelle padre a quelle figlio.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Ottiene la raccolta di tabelle contenute nel [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - true se la locale è stata impostata
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Legge lo schema XML e i dati nel [DataSet](../../com.aspose.words.net.system.data/dataset/) utilizzando il java.io.InputStream specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | java.io.InputStream | Un oggetto che deriva da java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Legge lo schema XML e i dati nel DataSet utilizzando il java.io.InputStream specificato e [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Lo Stream da cui leggere. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | Uno dei valori di [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Legge lo schema XML e i dati nel [DataSet](../../com.aspose.words.net.system.data/dataset/) utilizzando il file specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String | Il nome del file (incluso il percorso) da cui leggere. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Legge lo schema XML e i dati nel DataSet utilizzando il file specificato e [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xmlPath | java.lang.String | il file specificato |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Legge lo schema XML dal java.io.InputStream specificato nel [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | java.io.InputStream | Il java.io.InputStream da cui leggere. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Legge lo schema XML dal file specificato nel [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String | Il nome del file (incluso il percorso) da cui leggere. |

### reset() {#reset}
```
public void reset()
```


Ripristina il [DataSet](../../com.aspose.words.net.system.data/dataset/) al suo stato originale. Le classi derivate dovrebbero sovrascrivere [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) per ripristinare un [DataSet](../../com.aspose.words.net.system.data/dataset/) al suo stato originale.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Imposta il nome del corrente [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | java.lang.String | Il nome del [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Imposta un valore che indica se le regole di vincolo sono rispettate durante qualsiasi operazione di aggiornamento.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | true se le regole sono applicate; altrimenti false. Il valore predefinito è true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Imposta le informazioni locali utilizzate per confrontare le stringhe all'interno della tabella.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| locale | java.util.Locale | di questo data set |

