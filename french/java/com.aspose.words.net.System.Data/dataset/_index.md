---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words pour Java"
description: "Représente un cache de données en mémoire dans Java."
type: docs
weight: 24
url: /fr/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Représente un cache de données en mémoire.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataSet()](#DataSet) | Initialise une nouvelle instance de la classe [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Initialise une nouvelle instance de la classe DataSet avec des données provenant de Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Initialise une nouvelle instance de la classe DataSet avec des données provenant de Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Initialise une nouvelle instance d'une classe [DataSet](../../com.aspose.words.net.system.data/dataset/) avec le nom fourni. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Efface le [DataSet](../../com.aspose.words.net.system.data/dataset/) de toutes les données en supprimant toutes les lignes de toutes les tables. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Obtient le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/) actuel. |
| [getEnforceConstraints()](#getEnforceConstraints) | Obtient une valeur indiquant si les règles de contrainte sont respectées lors de toute opération de mise à jour. |
| [getNamespace()](#getNamespace) | Obtient l'espace de noms du [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | Récupère la collection de relations qui lient les tables et permettent la navigation des tables parentes vers les tables enfants. |
| [getTables()](#getTables) | Obtient la collection de tables contenues dans le [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Lit le schéma XML et les données dans le [DataSet](../../com.aspose.words.net.system.data/dataset/) en utilisant le java.io.InputStream spécifié. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Lit le schéma XML et les données dans le DataSet en utilisant le java.io.InputStream spécifié et le [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | Lit le schéma XML et les données dans le [DataSet](../../com.aspose.words.net.system.data/dataset/) en utilisant le fichier spécifié. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Lit le schéma XML et les données dans le DataSet en utilisant le fichier spécifié et le [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Lit le schéma XML depuis le java.io.InputStream spécifié dans le [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Lit le schéma XML depuis le fichier spécifié dans le [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | Réinitialise le [DataSet](../../com.aspose.words.net.system.data/dataset/) à son état d'origine. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Définit le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/) actuel. |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Définit une valeur indiquant si les règles de contrainte sont respectées lors de toute opération de mise à jour. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Définit les informations de paramètres régionaux utilisées pour comparer les chaînes dans la table. |
### DataSet() {#DataSet}
```
public DataSet()
```


Initialise une nouvelle instance de la classe [DataSet](../../com.aspose.words.net.system.data/dataset/).

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Initialise une nouvelle instance de la classe DataSet avec des données provenant de Connection. Les tables, relations, contraintes et index seront copiés dans DataSet.

Par défaut, aucun nom de schéma ne sera utilisé.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| connection | java.sql.Connection | qui contient les données de la base de données. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Initialise une nouvelle instance de la classe DataSet avec des données provenant de Connection. Les tables, relations, contraintes et index seront copiés dans DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

ou

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| connection | java.sql.Connection | qui contient les données de la base de données. |
| schemaName | java.lang.String | qui contient les tables à importer. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Initialise une nouvelle instance d'une classe [DataSet](../../com.aspose.words.net.system.data/dataset/) avec le nom fourni.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dataSetName | java.lang.String | Le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
booléen - vrai si le schéma a été lu
### clear() {#clear}
```
public void clear()
```


Efface le [DataSet](../../com.aspose.words.net.system.data/dataset/) de toutes les données en supprimant toutes les lignes de toutes les tables.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Obtient le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/) actuel.

**Returns:**
java.lang.String - Le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Obtient une valeur indiquant si les règles de contrainte sont respectées lors de toute opération de mise à jour.

**Returns:**
booléen - vrai si les règles sont appliquées ; sinon faux. La valeur par défaut est vraie.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtient l'espace de noms du [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - L'espace de noms du [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Récupère la collection de relations qui lient les tables et permettent la navigation des tables parentes vers les tables enfants.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Obtient la collection de tables contenues dans le [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
booléen - vrai si la locale a été définie
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Lit le schéma XML et les données dans le [DataSet](../../com.aspose.words.net.system.data/dataset/) en utilisant le java.io.InputStream spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream | Un objet qui dérive de java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Lit le schéma XML et les données dans le DataSet en utilisant le java.io.InputStream spécifié et le [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Le flux à partir duquel lire. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | Une des valeurs de [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Lit le schéma XML et les données dans le [DataSet](../../com.aspose.words.net.system.data/dataset/) en utilisant le fichier spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le nom de fichier (y compris le chemin) à partir duquel lire. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Lit le schéma XML et les données dans le DataSet en utilisant le fichier spécifié et le [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | le fichier spécifié |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Lit le schéma XML depuis le java.io.InputStream spécifié dans le [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream | Le java.io.InputStream à partir duquel lire. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Lit le schéma XML depuis le fichier spécifié dans le [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le nom de fichier (y compris le chemin) à partir duquel lire. |

### reset() {#reset}
```
public void reset()
```


Réinitialise le [DataSet](../../com.aspose.words.net.system.data/dataset/) à son état d'origine. Les sous‑classes doivent remplacer [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) pour restaurer un [DataSet](../../com.aspose.words.net.system.data/dataset/) à son état d'origine.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Définit le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/) actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Le nom du [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Définit une valeur indiquant si les règles de contrainte sont respectées lors de toute opération de mise à jour.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | vrai si les règles sont appliquées ; sinon faux. La valeur par défaut est vraie. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Définit les informations de paramètres régionaux utilisées pour comparer les chaînes dans la table.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| locale | java.util.Locale | de cet ensemble de données |

