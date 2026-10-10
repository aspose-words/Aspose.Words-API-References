---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words para Java"
description: "Representa una caché en memoria de datos en Java."
type: docs
weight: 24
url: /es/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Representa una caché de datos en memoria.
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DataSet()](#DataSet) | Inicializa una nueva instancia de la clase [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Inicializa una nueva instancia de la clase DataSet con datos tomados de Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Inicializa una nueva instancia de la clase DataSet con datos tomados de Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Inicializa una nueva instancia de una clase [DataSet](../../com.aspose.words.net.system.data/dataset/) con el nombre proporcionado. |
## Métodos

| Método | Descripción |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Limpia el [DataSet](../../com.aspose.words.net.system.data/dataset/) de cualquier dato eliminando todas las filas en todas las tablas. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Obtiene el nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/) actual. |
| [getEnforceConstraints()](#getEnforceConstraints) | Obtiene un valor que indica si se siguen las reglas de restricción al intentar cualquier operación de actualización. |
| [getNamespace()](#getNamespace) | Obtiene el espacio de nombres del [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | Obtenga la colección de relaciones que enlazan tablas y permiten la navegación de tablas padre a tablas hijo. |
| [getTables()](#getTables) | Obtiene la colección de tablas contenidas en el [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Lee el esquema XML y los datos en el [DataSet](../../com.aspose.words.net.system.data/dataset/) usando el java.io.InputStream especificado. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Lee el esquema XML y los datos en el DataSet usando el java.io.InputStream especificado y [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | Lee el esquema XML y los datos en el [DataSet](../../com.aspose.words.net.system.data/dataset/) usando el archivo especificado. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Lee el esquema XML y los datos en el DataSet usando el archivo especificado y [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Lee el esquema XML desde el java.io.InputStream especificado en el [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Lee el esquema XML desde el archivo especificado en el [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | Restablece el [DataSet](../../com.aspose.words.net.system.data/dataset/) a su estado original. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Establece el nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/) actual. |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Establece un valor que indica si se siguen las reglas de restricción al intentar cualquier operación de actualización. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Establece la información regional utilizada para comparar cadenas dentro de la tabla. |
### DataSet() {#DataSet}
```
public DataSet()
```


Inicializa una nueva instancia de la clase [DataSet](../../com.aspose.words.net.system.data/dataset/).

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Inicializa una nueva instancia de la clase DataSet con datos tomados de Connection. Las tablas, relaciones, restricciones e índices se copiarán en DataSet.

Por defecto no se utilizará ningún nombre de esquema.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| connection | java.sql.Connection | que contiene datos de la BD. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Inicializa una nueva instancia de la clase DataSet con datos tomados de Connection. Las tablas, relaciones, restricciones e índices se copiarán en DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

o

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| connection | java.sql.Connection | que contiene datos de la BD. |
| schemaName | java.lang.String | que contiene las tablas a importar. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Inicializa una nueva instancia de una clase [DataSet](../../com.aspose.words.net.system.data/dataset/) con el nombre proporcionado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dataSetName | java.lang.String | El nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - true si se leyó el esquema
### clear() {#clear}
```
public void clear()
```


Limpia el [DataSet](../../com.aspose.words.net.system.data/dataset/) de cualquier dato eliminando todas las filas en todas las tablas.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Obtiene el nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/) actual.

**Returns:**
java.lang.String - El nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Obtiene un valor que indica si se siguen las reglas de restricción al intentar cualquier operación de actualización.

**Returns:**
boolean - true si se aplican las reglas; de lo contrario false. El valor predeterminado es true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Obtiene el espacio de nombres del [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - El espacio de nombres del [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Obtenga la colección de relaciones que enlazan tablas y permiten la navegación de tablas padre a tablas hijo.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Obtiene la colección de tablas contenidas en el [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - true si se estableció locale.
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Lee el esquema XML y los datos en el [DataSet](../../com.aspose.words.net.system.data/dataset/) usando el java.io.InputStream especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream | Un objeto que deriva de java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Lee el esquema XML y los datos en el DataSet usando el java.io.InputStream especificado y [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlStream | java.io.InputStream | El Stream del cual leer. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | Uno de los valores de [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Lee el esquema XML y los datos en el [DataSet](../../com.aspose.words.net.system.data/dataset/) usando el archivo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El nombre de archivo (incluyendo la ruta) del cual leer. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Lee el esquema XML y los datos en el DataSet usando el archivo especificado y [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| xmlPath | java.lang.String | el archivo especificado |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Lee el esquema XML desde el java.io.InputStream especificado en el [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream | El java.io.InputStream del cual leer. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Lee el esquema XML desde el archivo especificado en el [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El nombre de archivo (incluyendo la ruta) del cual leer. |

### reset() {#reset}
```
public void reset()
```


Restablece el [DataSet](../../com.aspose.words.net.system.data/dataset/) a su estado original. Las subclases deben sobrescribir [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) para restaurar un [DataSet](../../com.aspose.words.net.system.data/dataset/) a su estado original.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Establece el nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/) actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | java.lang.String | El nombre del [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Establece un valor que indica si se siguen las reglas de restricción al intentar cualquier operación de actualización.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | true si se aplican las reglas; de lo contrario false. El valor predeterminado es true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Establece la información regional utilizada para comparar cadenas dentro de la tabla.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| locale | java.util.Locale | de este conjunto de datos |

